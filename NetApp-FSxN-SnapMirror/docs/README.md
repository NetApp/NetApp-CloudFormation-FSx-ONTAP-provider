# NetApp::FSxN::SnapMirror

Resource schema for SnapMirror.

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
        "<a href="#throttle" title="Throttle">Throttle</a>" : <i>Integer</i>,
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
    <a href="#throttle" title="Throttle">Throttle</a>: <i>Integer</i>
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

The File System Id of the Amazon FSx for NetApp ONTAP file system in which the resource is created.

_Required_: Yes

_Type_: String

_Pattern_: <code>^(fs-[0-9a-f]{8,18})$</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### LinkArn

_Required_: Yes

_Type_: String

_Pattern_: <code>^arn:aws(-(cn|us-gov))?:lambda:(([a-z]+-)+[0-9])?:([0-9]{12})?:function:[^.]+$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### FsxnDestinationInfo

_Required_: Yes

_Type_: <a href="fsxndestination.md">FsxnDestination</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnapMirrorSourceEndpoint

The endpoint of the SnapMirror relationship.

_Required_: Yes

_Type_: <a href="endpoint.md">Endpoint</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnapMirrorEndpoint

_Required_: Yes

_Type_: <a href="endpoint.md">Endpoint</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnapMirrorDestinationCreation

Use this object to provision the destination endpoint when establishing a SnapMirror relationship for a volume. For FlexGroup SnapMirror relationships, the source and destination FlexGroups must be spread over the same number of aggregates with the same number of constituents per aggregate.

_Required_: No

_Type_: <a href="snapmirrordestinationcreation.md">SnapMirrorDestinationCreation</a>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Policy

The SnapMirror policy to be used for the SnapMirror relationship.

_Required_: Yes

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Throttle

Throttle, in KBs per second. This "throttle" overrides the "throttle" set on the SnapMirror relationship's policy. If neither of these are set, defaults to 0, which is interpreted as unlimited.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### TransferSchedule

Schedule used to update asynchronous relationships. This "transfer_schedule" overrides the "transfer_schedule" set on the SnapMirror relationship's policy. Remove the property to for revert. Only cron schedules are supported for SnapMirror.

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

Reverse the direction of relationship, that is, make the source endpoint as the new destination endpoint and make the destination endpoint as the new source endpoint. Can be set during modify only.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
