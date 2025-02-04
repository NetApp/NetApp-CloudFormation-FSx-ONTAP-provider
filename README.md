# Amazon FSx for NetApp ONTAP CloudFormation Resource Types

This collection of [AWS CloudFormation resource types][1] allows management of ONTAP entities to be controlled using [AWS CloudFormation][2]. As for now the collection of resources is under private preview and can be activated using a key. To acquire a key, please email [NetApp](mailto:Ng-fsx-cloudformation@netapp.com?subject=CloudFormation%20Resource%20Provider%20key)

End-user documentation including:

* [Examples][20]
* supported GitHub resource types:

| Resource | Description | Documentation |
| --- | --- | --- |
| NetApp::FSxN::CifsShare | This resource type manages CIFS shares | [/NetApp-FSxN-CifsShare][4] |
| NetApp::FSxN::ClusterPeer | This resource type manages a cluster peer | [/NetApp-FSxN-ClusterPeer][5] |
| NetApp::FSxN::ExportPolicy | This resource type manages an export policy | [/NetApp-FSxN-ExportPolicy][6] |
| NetApp::FSxN::IGroup | This resource type manages an igroup | [/NetApp-FSxN-IGroup][7] |
| NetApp::FSxN::SnapMirror | This resource type manages a SnapMirror relationship | [/NetApp-FSxN-SnapMirror][8] |
| NetApp::FSxN::Snapshot | This resource type manages a volume snapshot | [/NetApp-FSxN-Snapshot][9] |
| NetApp::FSxN::SnapshotPolicy | This resource type manages a snapshot policy | [/NetApp-FSxN-SnapshotPolicy][10] |
| NetApp::FSxN::SvmPeer | This resource type manages an SVM peer | [/NetApp-FSxN-SvmPeer][16] |
| NetApp::FSxN::Volume | This resource type manages a volume | [/NetApp-FSxN-Volume][17] |
* Resource import and drifting not supported.

## Prerequisites

* [AWS Account][14]
* [AWS CLI][15]
* Preview Key
* FSxN Credentials Stored In AWS Secret Manager
* Execution Role
* [Resource Activation][19]
* Deploy a Link

A Link is an entity (Lambda) that act as a proxy between the CloudFormation service and the FSx for ONTAP file systems. The Link must be deployed in a VPC that has connectivity to the management endpoint of the FSx for ONTAP file systems. A single Link can be used for all FSx for ONTAP file systems if there is connectivity for all resources.

## Preview Key
As for now the collection of resources is under private preview and can be activated using a key. To acquire a key, please email [NetApp](mailto:Ng-fsx-cloudformation@netapp.com?subject=CloudFormation%20Resource%20Provider%20key)

## Credentials:
FSx for ONTAP file systems credentials are required for the link communication. Credentials required to stored in AWS Secret Manger Service in the following formats:
* ```Username```:```Password```
* ```Password``` (assuming ```fsxadmin``` default user)

After you have your credentials stored [create your AWS stack][12] and use the secret ARN and secret Key input for ```SecretArn``` and ```SecretKey``` input parameters.

## Execution Role
AWS Resource types requires [Activation Execution IAM Role][18].
The following Execution Role YAML can be deployed in a stack and used for the entire collection of resources.

```yaml
---
AWSTemplateFormatVersion: "2010-09-09"
Description: >
  This CloudFormation template creates a role assumed by CloudFormation
  during CRUDL operations to mutate resources on behalf of the customer.

Resources:
  ExecutionRole:
    Type: AWS::IAM::Role
    Properties:
      MaxSessionDuration: 8400
      AssumeRolePolicyDocument:
        Version: '2012-10-17'
        Statement:
          - Effect: Allow
            Principal:
              Service: resources.cloudformation.amazonaws.com
            Action: sts:AssumeRole
      Path: "/"
      Policies:
        - PolicyName: ResourceTypePolicy
          PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Effect: Allow
                Action:
                  - "fsx:DescribeFileSystems"
                  - "lambda:InvokeFunction"
                  - "secretsmanager:GetSecretValue"
                Resource: "*"
Outputs:
  ExecutionRoleArn:
    Value:
      Fn::GetAtt: ExecutionRole.Arn
```
* Specific Resource Role with a strict condition in the assume policy can be found on each resource docs named under ```resource-role.yaml``` 

## Step 1: Activate Link Module

1. Sign in to the [AWS Management Console][11] with your account and navigate to CloudFormation.

2. Select "Public extensions" from the left-hand pane and filter by Extension type by Module and Publisher by "Third Party".

3. Use the search bar to filter by the "NetApp" prefix.

4. Select the Link module to view more information about its schema and click **Activate**.

5. On the **Extension details** page, specify:

* Extension name
* Automatic updates for minor version releases

6. After you have your Link module configured, [create your AWS stack][12] and use the ARN as input for the ```LinkArn``` input parameter.

## Step 2: Activate ONTAP resources

1. Sign in to the [AWS Management Console][11] with your account and navigate to CloudFormation.

2. Select "Public extensions" from the left-hand pane and filter Publisher by "Third Party".

3. Use the search bar to filter by the "NetApp" prefix.

  Note: All official  Netapp resources begin with `NetApp::FSxN` and specify that they are `Published by NetApp`.

4. Select the desired resource name to view more information about its schema and click **Activate**.

5. On the **Extension details** page, specify:

* Extension name
* Execution role ARN
* Automatic updates for minor version releases
* Configuration (PreviewKey)

6. In your terminal, specify the configuration data for the registered NetApp CloudFormation resource type, in the given account and region by using the **SetTypeConfiguration** operation:

  For example:

  ```Bash
  aws cloudformation set-type-configuration \
  --region us-west-2 --type RESOURCE \
  --type-name NetApp::FSxN::CifsShare \
  --configuration-alias default \
  --configuration "{\"PreviewKey\":\"YOURPREVIEWKEY\"}"
  ```

7. After you have your resource configured, [create your AWS stack][12] that includes any of the activated ONTAP resources.

For more information about available commands and workflows, see the official [AWS documentation][13].

## Supported regions

The NetApp ONTAP CloudFormation resources are available on the CloudFormation Public Registry in the following regions:

| Code            | Name                      |
|-----------------|---------------------------|
| us-east-1       | US East (N. Virginia)     |
| us-east-2       | US East (Ohio)            |
| us-west-1       | US West (N. California)   |
| us-west-2       | US West (Oregon)          |
| af-south-1      | Africa (Cape Town)        |
| ap-east -1      | Asia Pacific (Hong Kong)  |
| ap-south-1      | Asia Pacific (Mumbai)     |
| ap-south-2      | Asia Pacific (Hyderabad)  |
| ap-northeast-1  | Asia Pacific (Tokyo)      |
| ap-northeast-2  | Asia Pacific (Seoul)      |
| ap-northeast-3  | Asia Pacific (Osaka)      |
| ap-southeast-1  | Asia Pacific (Singapore)  |
| ap-southeast-2  | Asia Pacific (Sydney)     |
| ap-southeast-3  | Asia Pacific (Jakarta)    |
| ap-southeast-4  | Asia Pacific (Melbourne)  |
| ca-central-1    | Canada (Central)          |
| eu-central-1    | Europe (Frankfurt)        |
| eu-central-2    | Europe (Zurich)           |
| eu-west-1       | Europe (Ireland)          |
| eu-west-2       | Europe (London)           |
| eu-west-3       | Europe (Paris)            |
| eu-north-1      | Europe (Stockholm)        |
| eu-south-1      | Europe (Milan)            |
| eu-south-2      | Europe (Spain)            |
| il-central-1    | Israel (Tel Aviv)         |
| me-south-1      | Middle East (Bahrain)     |
| me-central-1    | Middle East (UAE)         |
| sa-east-1       | South America (São Paulo) |

## Examples

### Example 1: Shows how to create an igroup

```yaml
---
AWSTemplateFormatVersion: '2010-09-09'
Description: Shows how to create an IGroup
Resources:
  IGroup:
    Type: NetApp::FSxN::IGroup
    Properties:
      FsxAdminPasswordSource:
        Secret:
          SecretArn: !Ref SecretArn
          SecretKey: !Ref SecretKey
      FileSystemId: !Ref FSXIdSource
      LinkArn: !Ref LinkArn
      Name: igroupdemo
      Initiators:
        - Name: iqn.2022-10.com.storage:server
      SVM:
        Name: !Ref SVMName
      OsType: linux
    DeletionPolicy: Delete
```

### Example 2: Shows how to create a volume

```yaml
---
AWSTemplateFormatVersion: '2010-09-09'
Description: Shows how to create a volume
Resources:
  Volume:
    Type: NetApp::FSxN::Volume
    Properties:
      FsxAdminPasswordSource:
        Secret:
          SecretArn: !Ref SecretArn
          SecretKey: !Ref SecretKey
      FileSystemId: !Ref FSXIdSource
      LinkArn: !Ref LinkArn
      Name: !Ref VolumeName
      SVM:
        Name: !Ref SVMName
      Size: 2147483648000
      Aggregates:
        - aggr1
    DeletionPolicy: Delete
```

### Example 3: Shows how to create a LUN

```yaml
---
AWSTemplateFormatVersion: '2010-09-09'
Description: Shows how to create a lun.
Resources:
  Lun:
    Type: NetApp::FSxN::Lun
    Properties:
      FsxAdminPasswordSource:
        Secret:
          SecretArn: !Ref SecretArn
          SecretKey: !Ref SecretKey
      FileSystemId: !Ref FSXIdSource
      LinkArn: !Ref LinkArn
      SVM:
        Name: !Ref SVMName
      OsType: aix
      Name: !Sub '/vol/${VolumeName}/${LunName}'
      Size: 4096
      IGroups:
        - igrouptest
    DependsOn:
      - Volume
      - IGroup
    DeletionPolicy: Delete
```

[1]: https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-types.html
[2]: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html
[4]: ./NetApp-FSxN-CifsShare/
[5]: ./NetApp-FSxN-ClusterPeer/
[6]: ./NetApp-FSxN-ExportPolicy/
[7]: ./NetApp-FSxN-IGroup/
[8]: ./NetApp-FSxN-SnapMirror/
[9]: ./NetApp-FSxN-Snapshot/
[10]: ./NetApp-FSxN-SnapshotPolicy/
[11]: https://aws.amazon.com/console/
[12]: https://console.aws.amazon.com/cloudformation/home
[13]: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html
[14]: https://aws.amazon.com/account/
[15]: https://aws.amazon.com/cli/api-key-auth/
[16]: ./NetApp-FSxN-SvmPeer/
[17]: ./NetApp-FSxN-Volume/
[18]: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html#registry-public-enable-execution-role
[19]: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public-activate-extension.html
[20]: Examples/
