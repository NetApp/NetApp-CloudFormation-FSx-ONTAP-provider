# NetApp::FSxN::Volume

Resource schema for Volume.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::Volume",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#svm" title="SVM">SVM</a>" : <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>,
        "<a href="#name" title="Name">Name</a>" : <i>String</i>,
        "<a href="#size" title="Size">Size</a>" : <i>Double</i>,
        "<a href="#ontaptags" title="ONTAPTags">ONTAPTags</a>" : <i>[ <a href="ontaptag.md">ONTAPTag</a>, ... ]</i>,
        "<a href="#aggregates" title="Aggregates">Aggregates</a>" : <i>[ String, ... ]</i>,
        "<a href="#constituentsperaggregate" title="ConstituentsPerAggregate">ConstituentsPerAggregate</a>" : <i>Integer</i>,
        "<a href="#snapshotpolicy" title="SnapshotPolicy">SnapshotPolicy</a>" : <i>String</i>,
        "<a href="#encryption" title="Encryption">Encryption</a>" : <i>Boolean</i>,
        "<a href="#type" title="Type">Type</a>" : <i>String</i>,
        "<a href="#style" title="Style">Style</a>" : <i>String</i>,
        "<a href="#state" title="State">State</a>" : <i>String</i>,
        "<a href="#antiransomwarestate" title="AntiRansomwareState">AntiRansomwareState</a>" : <i>String</i>,
        "<a href="#efficiency" title="Efficiency">Efficiency</a>" : <i><a href="efficiency.md">Efficiency</a></i>,
        "<a href="#snaplock" title="Snaplock">Snaplock</a>" : <i><a href="snaplock.md">Snaplock</a></i>,
        "<a href="#tiering" title="Tiering">Tiering</a>" : <i><a href="tiering.md">Tiering</a></i>,
        "<a href="#clone" title="Clone">Clone</a>" : <i><a href="clone.md">Clone</a></i>,
        "<a href="#nas" title="NAS">NAS</a>" : <i><a href="nas.md">NAS</a></i>,
        "<a href="#autosize" title="Autosize">Autosize</a>" : <i><a href="autosize.md">Autosize</a></i>
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::Volume
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#svm" title="SVM">SVM</a>: <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>
    <a href="#name" title="Name">Name</a>: <i>String</i>
    <a href="#size" title="Size">Size</a>: <i>Double</i>
    <a href="#ontaptags" title="ONTAPTags">ONTAPTags</a>: <i>
      - <a href="ontaptag.md">ONTAPTag</a></i>
    <a href="#aggregates" title="Aggregates">Aggregates</a>: <i>
      - String</i>
    <a href="#constituentsperaggregate" title="ConstituentsPerAggregate">ConstituentsPerAggregate</a>: <i>Integer</i>
    <a href="#snapshotpolicy" title="SnapshotPolicy">SnapshotPolicy</a>: <i>String</i>
    <a href="#encryption" title="Encryption">Encryption</a>: <i>Boolean</i>
    <a href="#type" title="Type">Type</a>: <i>String</i>
    <a href="#style" title="Style">Style</a>: <i>String</i>
    <a href="#state" title="State">State</a>: <i>String</i>
    <a href="#antiransomwarestate" title="AntiRansomwareState">AntiRansomwareState</a>: <i>String</i>
    <a href="#efficiency" title="Efficiency">Efficiency</a>: <i><a href="efficiency.md">Efficiency</a></i>
    <a href="#snaplock" title="Snaplock">Snaplock</a>: <i><a href="snaplock.md">Snaplock</a></i>
    <a href="#tiering" title="Tiering">Tiering</a>: <i><a href="tiering.md">Tiering</a></i>
    <a href="#clone" title="Clone">Clone</a>: <i><a href="clone.md">Clone</a></i>
    <a href="#nas" title="NAS">NAS</a>: <i><a href="nas.md">NAS</a></i>
    <a href="#autosize" title="Autosize">Autosize</a>: <i><a href="autosize.md">Autosize</a></i>
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

#### SVM

_Required_: Yes

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Name

Volume name. The name of volume must start with an alphabetic character (a to z or A to Z) or an underscore (\_). The name must be 197 or fewer characters in length for FlexGroups, and 203 or fewer characters in length for all other types of volumes. Volume names must be unique within an SVM.

_Required_: Yes

_Type_: String

_Pattern_: <code>^[a-zA-Z\_][a-zA-Z0-9_]{0,202}$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Size

Physical size of the volume, in bytes. The minimum size for a FlexVol volume is 20MB and the minimum size for a FlexGroup volume is 200MB per constituent. The recommended size for a FlexGroup volume is a minimum of 100GB per constituent. For all volumes, the default size is equal to the minimum size.

_Required_: No

_Type_: Double

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ONTAPTags

_Required_: No

_Type_: List of <a href="ontaptag.md">ONTAPTag</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Aggregates

Aggregate name list hosting the volume.

_Required_: No

_Type_: List of String

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### ConstituentsPerAggregate

Specifies the number of times to iterate over the aggregates when creating or expanding a FlexGroup volume.

_Required_: No

_Type_: Integer

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### SnapshotPolicy

Snapshot policy name.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Encryption

Creates an encrypted or an unencrypted volume.

_Required_: No

_Type_: Boolean

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Type

Type of the volume.

_Required_: No

_Type_: String

_Allowed Values_: <code>rw</code> | <code>dp</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Style

The style of the volume.

_Required_: No

_Type_: String

_Allowed Values_: <code>flexvol</code> | <code>flexgroup</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### State

Volume state. Client access is supported only when volume is online and junctioned. Taking volume to offline or restricted state removes its junction path and blocks client access. When volume is in restricted state some operations like parity reconstruction and iron on commit are allowed. The 'mixed' state applies to FlexGroup volumes only and cannot be specified as a target state. An 'error' state implies that the volume is not in a state to serve data.

_Required_: No

_Type_: String

_Allowed Values_: <code>offline</code> | <code>online</code> | <code>restricted</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### AntiRansomwareState

Anti-ransomware state.

_Required_: No

_Type_: String

_Allowed Values_: <code>disabled</code> | <code>dry_run</code> | <code>enabled</code> | <code>paused</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Efficiency

_Required_: No

_Type_: <a href="efficiency.md">Efficiency</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Snaplock

_Required_: No

_Type_: <a href="snaplock.md">Snaplock</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Tiering

_Required_: No

_Type_: <a href="tiering.md">Tiering</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Clone

_Required_: No

_Type_: <a href="clone.md">Clone</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### NAS

_Required_: No

_Type_: <a href="nas.md">NAS</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Autosize

_Required_: No

_Type_: <a href="autosize.md">Autosize</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
