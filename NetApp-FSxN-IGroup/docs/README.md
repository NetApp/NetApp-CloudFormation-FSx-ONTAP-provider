# NetApp::FSxN::IGroup

Resource schema for IGroup.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::IGroup",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#name" title="Name">Name</a>" : <i>String</i>,
        "<a href="#initiators" title="Initiators">Initiators</a>" : <i>[ <a href="initiator.md">Initiator</a>, ... ]</i>,
        "<a href="#ostype" title="OsType">OsType</a>" : <i>String</i>,
        "<a href="#svm" title="SVM">SVM</a>" : <i><a href="svm.md">SVM</a></i>
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::IGroup
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#name" title="Name">Name</a>: <i>String</i>
    <a href="#initiators" title="Initiators">Initiators</a>: <i>
      - <a href="initiator.md">Initiator</a></i>
    <a href="#ostype" title="OsType">OsType</a>: <i>String</i>
    <a href="#svm" title="SVM">SVM</a>: <i><a href="svm.md">SVM</a></i>
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

#### Name

_Required_: No

_Type_: String

_Minimum Length_: <code>1</code>

_Maximum Length_: <code>96</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Initiators

The initiators that are attached to the initiator group

_Required_: No

_Type_: List of <a href="initiator.md">Initiator</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### OsType

The host operating system of the initiator group. All initiators in the group should be hosts of the same operating system

_Required_: No

_Type_: String

_Allowed Values_: <code>aix</code> | <code>hpux</code> | <code>hyper_v</code> | <code>linux</code> | <code>netware</code> | <code>openvms</code> | <code>solaris</code> | <code>solaris_efi</code> | <code>vmware</code> | <code>windows</code> | <code>windows_2008</code> | <code>windows_gpt</code> | <code>xen</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SVM

_Required_: No

_Type_: <a href="svm.md">SVM</a>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
