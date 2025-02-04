# NetApp::FSxN::Volume

A volume is a logical storage unit which provides flexible space for data files, snapshots, and block devices. The NetApp:FSxN custom resource allows you to configure and manage FSX for ONTAP volumes by specifying parameters such as volume name, size, storage efficiency, export policies, and other attributes. To use this resource, you must create the Link module. Once activated, you will need a preview key to consume this resource. Please reach out to Ng-fsx-cloudformation@netapp.com to get the key.

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

#### SVM

_Required_: Yes

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Name

Volume name. The name of volume must start with an alphabetic character (a to z or A to Z) or an underscore (_). The name must be 197 or fewer characters in length for FlexGroups, and 203 or fewer characters in length for all other types of volumes. Volume names must be unique within an SVM.

_Required_: Yes

_Type_: String

_Pattern_: <code>^[a-zA-Z_][a-zA-Z0-9_]{0,202}$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Size

Physical size of the volume, in bytes. The minimum size for a FlexVol volume is 20MB and the minimum size for a FlexGroup volume is 200MB per constituent. The recommended size for a FlexGroup volume is a minimum of 100GB per constituent. For all volumes, the default size is equal to the minimum size.

_Required_: No

_Type_: Double

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ONTAPTags

Tags associated with the ONTAP volume.

_Required_: No

_Type_: List of <a href="ontaptag.md">ONTAPTag</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Aggregates

List of aggregate names that host the volume.

_Required_: No

_Type_: List of String

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### ConstituentsPerAggregate

Specifies the number of times to iterate constituents over the aggregates when creating or expanding a FlexGroup volume.

_Required_: No

_Type_: Integer

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### SnapshotPolicy

Snapshot policy name.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Encryption

Indicates if the volume is encrypted.

_Required_: No

_Type_: Boolean

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Type

The type of volume (e.g., read-write or data protection).

_Required_: No

_Type_: String

_Allowed Values_: <code>rw</code> | <code>dp</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Style

The style of the volume (e.g., FlexVol or FlexGroup).

_Required_: No

_Type_: String

_Allowed Values_: <code>flexvol</code> | <code>flexgroup</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### State

The state of the volume (e.g., online, offline, restricted). Client access is supported only when volume is online and connected to its junction path. Taking volume to offline or restricted state removes its junction path and blocks client access.

_Required_: No

_Type_: String

_Allowed Values_: <code>offline</code> | <code>online</code> | <code>restricted</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### AntiRansomwareState

The anti-ransomware state of the volume.

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
