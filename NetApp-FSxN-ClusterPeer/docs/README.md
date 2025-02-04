# NetApp::FSxN::ClusterPeer

A cluster peer establishes a trusted network relationship between two FSx for ONTAP file systems, allowing them to securely communicate and exchange data. The relationship enables encrypted, authenticated data replication. The cluster peer can be used for disaster recovery across clusters in different regions, which provides flexibility for data protection and high availability. Once activated, you will need a preview key to consume this resource. Please reach out to Ng-fsx-cloudformation@netapp.com to get the key. To use this resource, you would need to first create the Link module.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::ClusterPeer",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#fsxndestinationinfo" title="FsxnDestinationInfo">FsxnDestinationInfo</a>" : <i><a href="fsxndestination.md">FsxnDestination</a></i>,
        "<a href="#sourceclusterpeer" title="SourceClusterPeer">SourceClusterPeer</a>" : <i><a href="clusterpeerinfo.md">ClusterPeerInfo</a></i>,
        "<a href="#destinationclusterpeer" title="DestinationClusterPeer">DestinationClusterPeer</a>" : <i><a href="clusterpeerinfo.md">ClusterPeerInfo</a></i>,
        "<a href="#encryption" title="Encryption">Encryption</a>" : <i>String</i>
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::ClusterPeer
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#fsxndestinationinfo" title="FsxnDestinationInfo">FsxnDestinationInfo</a>: <i><a href="fsxndestination.md">FsxnDestination</a></i>
    <a href="#sourceclusterpeer" title="SourceClusterPeer">SourceClusterPeer</a>: <i><a href="clusterpeerinfo.md">ClusterPeerInfo</a></i>
    <a href="#destinationclusterpeer" title="DestinationClusterPeer">DestinationClusterPeer</a>: <i><a href="clusterpeerinfo.md">ClusterPeerInfo</a></i>
    <a href="#encryption" title="Encryption">Encryption</a>: <i>String</i>
</pre>

## Properties

#### FsxAdminPasswordSource

_Required_: Yes

_Type_: <a href="passwordsource.md">PasswordSource</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### FileSystemId

The file system ID of the Amazon FSx for NetApp ONTAP file system in which the resource is created.

_Required_: Yes

_Type_: String

_Pattern_: <code>^(fs-[0-9a-f]{8,18})$</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### LinkArn

The ARN of the AWS Lambda function that will be invoked to manage the resource.

_Required_: Yes

_Type_: String

_Pattern_: <code>^arn:aws(-(cn|us-gov))?:lambda:(([a-z]+-)+[0-9])?:([0-9]{12})?:function:[^.]+$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### FsxnDestinationInfo

_Required_: Yes

_Type_: <a href="fsxndestination.md">FsxnDestination</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SourceClusterPeer

_Required_: No

_Type_: <a href="clusterpeerinfo.md">ClusterPeerInfo</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### DestinationClusterPeer

_Required_: No

_Type_: <a href="clusterpeerinfo.md">ClusterPeerInfo</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Encryption

Encryption mechanism of the communication channel between the two peers.

_Required_: No

_Type_: String

_Allowed Values_: <code>none</code> | <code>tls_psk</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
