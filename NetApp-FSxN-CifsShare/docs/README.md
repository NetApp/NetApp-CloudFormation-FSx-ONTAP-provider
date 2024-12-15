# NetApp::FSxN::CifsShare

Resource schema for Cifs Shares and Cifs Shares ACLs.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::CifsShare",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#name" title="Name">Name</a>" : <i>String</i>,
        "<a href="#svm" title="SVM">SVM</a>" : <i><a href="svm.md">SVM</a></i>,
        "<a href="#path" title="Path">Path</a>" : <i>String</i>,
        "<a href="#comment" title="Comment">Comment</a>" : <i>String</i>,
        "<a href="#acls" title="ACLs">ACLs</a>" : <i>[ <a href="cifsshareacl.md">CifsShareAcl</a>, ... ]</i>,
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::CifsShare
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#name" title="Name">Name</a>: <i>String</i>
    <a href="#svm" title="SVM">SVM</a>: <i><a href="svm.md">SVM</a></i>
    <a href="#path" title="Path">Path</a>: <i>String</i>
    <a href="#comment" title="Comment">Comment</a>: <i>String</i>
    <a href="#acls" title="ACLs">ACLs</a>: <i>
      - <a href="cifsshareacl.md">CifsShareAcl</a></i>
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

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Name

Name of the CIFS share.

_Required_: Yes

_Type_: String

_Pattern_: <code>^[a-zA-Z0-9_-]{1,80}$</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### SVM

_Required_: Yes

_Type_: <a href="svm.md">SVM</a>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Path

Path in the owning SVM namespace that is shared through this share.

_Required_: Yes

_Type_: String

_Pattern_: <code>^/[a-zA-Z0-9_-]{1,256}$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Comment

Text comment about the CIFS share.

_Required_: No

_Type_: String

_Minimum Length_: <code>1</code>

_Maximum Length_: <code>256</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ACLs

Share permissions that users and groups have on the CIFS share.

_Required_: No

_Type_: List of <a href="cifsshareacl.md">CifsShareAcl</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
