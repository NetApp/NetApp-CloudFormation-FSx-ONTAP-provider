# NetApp::FSxN::SnapMirror

FSx for ONTAP provides SnapMirror, an embedded data replication technology that allows for the efficient transfer of data between two file systems. SnapMirror replicates data by creating point-in-time copies of the data. It is used for data protection, disaster recovery, and business continuity by ensuring that up-to-date copies of data are available at remote locations. To use SnapMirror, you must set up cluster peering and SVM peering between the source and target FSx for ONTAP file systems. Once activated, you will need a preview key to consume this resource. Please reach out to Ng-fsx-cloudformation@netapp.com to get the key. To use this resource, you would need to first create the Link module.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::SnapMirror",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#fsxndestinationinfo" title="FsxnDestinationInfo">FsxnDestinationInfo</a>" : <i><a href="fsxndestination.md">FsxnDestination</a></i>,
        "<a href="#snapmirrorsourceendpoint" title="SnapMirrorSourceEndpoint">SnapMirrorSourceEndpoint</a>" : <i><a href="endpoint.md">Endpoint</a></i>,
        "<a href="#snapmirrorendpoint" title="SnapMirrorEndpoint">SnapMirrorEndpoint</a>" : <i><a href="endpoint.md">Endpoint</a></i>,
        "<a href="#snapmirrordestinationcreation" title="SnapMirrorDestinationCreation">SnapMirrorDestinationCreation</a>" : <i><a href="snapmirrordestinationcreation.md">SnapMirrorDestinationCreation</a></i>,
        "<a href="#policy" title="Policy">Policy</a>" : <i>String</i>,
        "<a href="#throttle" title="Throttle">Throttle</a>" : <i>Double</i>,
        "<a href="#transferschedule" title="TransferSchedule">TransferSchedule</a>" : <i>String</i>,
        "<a href="#stateaction" title="StateAction">StateAction</a>" : <i>String</i>,
        "<a href="#reverse" title="Reverse">Reverse</a>" : <i>Boolean</i>,
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::SnapMirror
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#fsxndestinationinfo" title="FsxnDestinationInfo">FsxnDestinationInfo</a>: <i><a href="fsxndestination.md">FsxnDestination</a></i>
    <a href="#snapmirrorsourceendpoint" title="SnapMirrorSourceEndpoint">SnapMirrorSourceEndpoint</a>: <i><a href="endpoint.md">Endpoint</a></i>
    <a href="#snapmirrorendpoint" title="SnapMirrorEndpoint">SnapMirrorEndpoint</a>: <i><a href="endpoint.md">Endpoint</a></i>
    <a href="#snapmirrordestinationcreation" title="SnapMirrorDestinationCreation">SnapMirrorDestinationCreation</a>: <i><a href="snapmirrordestinationcreation.md">SnapMirrorDestinationCreation</a></i>
    <a href="#policy" title="Policy">Policy</a>: <i>String</i>
    <a href="#throttle" title="Throttle">Throttle</a>: <i>Double</i>
    <a href="#transferschedule" title="TransferSchedule">TransferSchedule</a>: <i>String</i>
    <a href="#stateaction" title="StateAction">StateAction</a>: <i>String</i>
    <a href="#reverse" title="Reverse">Reverse</a>: <i>Boolean</i>
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

#### SnapMirrorSourceEndpoint

_Required_: Yes

_Type_: <a href="endpoint.md">Endpoint</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnapMirrorEndpoint

_Required_: Yes

_Type_: <a href="endpoint.md">Endpoint</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnapMirrorDestinationCreation

_Required_: No

_Type_: <a href="snapmirrordestinationcreation.md">SnapMirrorDestinationCreation</a>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Policy

The SnapMirror policy to be used for the SnapMirror relationship.

_Required_: Yes

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Throttle

Throttle, in KBs per second. This 'throttle' overrides the 'throttle' set on the SnapMirror relationship's policy. If neither of these are set, the throttle defaults to 0, which is interpreted as unlimited.

_Required_: No

_Type_: Double

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### TransferSchedule

Schedule used to update asynchronous relationships. This 'transfer_schedule' overrides the 'transfer_schedule' set on the SnapMirror relationship's policy. Remove the property to revert. Only cron schedules are supported for SnapMirror.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### StateAction

Setting state of the relationship. Can be set during modify only.

_Required_: No

_Type_: String

_Allowed Values_: <code>broken_off</code> | <code>paused</code> | <code>snapmirrored</code> | <code>in_sync</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Reverse

Reverse the direction of relationship by making the source endpoint as the new destination endpoint and making the destination endpoint as the new source endpoint. Can be set during modify only.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
