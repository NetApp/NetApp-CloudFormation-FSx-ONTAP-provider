# NetApp::FSxN::Lun

Resource schema for Lun.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::Lun",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#name" title="Name">Name</a>" : <i>String</i>,
        "<a href="#qospolicyname" title="QosPolicyName">QosPolicyName</a>" : <i>String</i>,
        "<a href="#size" title="Size">Size</a>" : <i>Integer</i>,
        "<a href="#igroups" title="IGroups">IGroups</a>" : <i>[ String, ... ]</i>,
        "<a href="#svm" title="SVM">SVM</a>" : <i><a href="svm.md">SVM</a></i>,
        "<a href="#ostype" title="OsType">OsType</a>" : <i>String</i>
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::Lun
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#name" title="Name">Name</a>: <i>String</i>
    <a href="#qospolicyname" title="QosPolicyName">QosPolicyName</a>: <i>String</i>
    <a href="#size" title="Size">Size</a>: <i>Integer</i>
    <a href="#igroups" title="IGroups">IGroups</a>: <i>
      - String</i>
    <a href="#svm" title="SVM">SVM</a>: <i><a href="svm.md">SVM</a></i>
    <a href="#ostype" title="OsType">OsType</a>: <i>String</i>
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

The fully qualified path name of the LUN composed of a '/vol' prefix, the volume name, and base name of the LUN. example: /vol/volume1/lun1

_Required_: Yes

_Type_: String

_Pattern_: <code>^/vol/[a-zA-Z0-9_-]+/[a-zA-Z0-9_-]+$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### QosPolicyName

The name of the QoS policy for the LUN.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Size

Size of the LUN. Required when creating a non-clone LUN and disallowed when creating a clone of an existing LUN. A clone's size is taken from the source LUN.

_Required_: Yes

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### IGroups

The initiator groups mapped to this LUN

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SVM

_Required_: Yes

_Type_: <a href="svm.md">SVM</a>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### OsType

The host operating system of the initiator group. All initiators in the group should be hosts of the same operating system

_Required_: Yes

_Type_: String

_Allowed Values_: <code>aix</code> | <code>hpux</code> | <code>hyper_v</code> | <code>linux</code> | <code>netware</code> | <code>openvms</code> | <code>solaris</code> | <code>solaris_efi</code> | <code>vmware</code> | <code>windows</code> | <code>windows_2008</code> | <code>windows_gpt</code> | <code>xen</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
