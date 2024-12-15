# NetApp::FSxN::SvmPeer FsxnDestination

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
    "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
    "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
<a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
<a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
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

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### LinkArn

The ARN of the Lambda function that will be invoked to create the SVM peer relationship.

_Required_: Yes

_Type_: String

_Pattern_: <code>^arn:aws(-(cn|us-gov))?:lambda:(([a-z]+-)+[0-9])?:([0-9]{12})?:function:[^.]+$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

