# NetApp::FSxN::Snapshot

A snapshot creates a read-only copy of a volume or LUN at a specific time. It allows users to restore files or volumes if data is deleted, corrupted, or changed. Snapshots efficiently store only the changes made after the snapshot, making them ideal for data protection and recovery. Once activated, you need a preview key to consume this resource. Please reach out to Ng-fsx-cloudformation@netapp.com to get the key. To use this resource, you must first create the Link module.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::Snapshot",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#volume" title="Volume">Volume</a>" : <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>,
        "<a href="#svm" title="SVM">SVM</a>" : <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>,
        "<a href="#name" title="Name">Name</a>" : <i>String</i>,
        "<a href="#snapmirrorlabel" title="SnapmirrorLabel">SnapmirrorLabel</a>" : <i>String</i>,
        "<a href="#comment" title="Comment">Comment</a>" : <i>String</i>,
        "<a href="#expirytime" title="ExpiryTime">ExpiryTime</a>" : <i>String</i>,
        "<a href="#snaplockexpirytime" title="SnaplockExpiryTime">SnaplockExpiryTime</a>" : <i>String</i>
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::Snapshot
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#volume" title="Volume">Volume</a>: <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>
    <a href="#svm" title="SVM">SVM</a>: <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>
    <a href="#name" title="Name">Name</a>: <i>String</i>
    <a href="#snapmirrorlabel" title="SnapmirrorLabel">SnapmirrorLabel</a>: <i>String</i>
    <a href="#comment" title="Comment">Comment</a>: <i>String</i>
    <a href="#expirytime" title="ExpiryTime">ExpiryTime</a>: <i>String</i>
    <a href="#snaplockexpirytime" title="SnaplockExpiryTime">SnaplockExpiryTime</a>: <i>String</i>
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

#### Volume

_Required_: Yes

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SVM

_Required_: Yes

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Name

The name of the snapshot copy to be created.

_Required_: Yes

_Type_: String

_Minimum Length_: <code>1</code>

_Maximum Length_: <code>255</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnapmirrorLabel

Label for SnapMirror operations.

_Required_: No

_Type_: String

_Minimum Length_: <code>1</code>

_Maximum Length_: <code>31</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Comment

Comment associated with the snapshot copy.

_Required_: No

_Type_: String

_Minimum Length_: <code>1</code>

_Maximum Length_: <code>255</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ExpiryTime

Date time format UTC (YYYY-MM-DD hh:mm:ss).

_Required_: No

_Type_: String

_Pattern_: <code>^((\d{4})-(0[1-9]|1[0-2])-([0-2]\d|3[01]) ([01]\d|2[0-4]):([0-5]\d):([0-5]\d))$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnaplockExpiryTime

Date time format UTC (YYYY-MM-DD hh:mm:ss).

_Required_: No

_Type_: String

_Pattern_: <code>^((\d{4})-(0[1-9]|1[0-2])-([0-2]\d|3[01]) ([01]\d|2[0-4]):([0-5]\d):([0-5]\d))$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
