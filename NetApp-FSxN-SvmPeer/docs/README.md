# NetApp::FSxN::SvmPeer

A storage VM (SVM) peer is a relationship established between two SVMs from different FSX for ONTAP file systems, enabling the sharing of resources and data across file systems. Once activated, you will need a preview key to consume this resource. Please reach out to Ng-fsx-cloudformation@netapp.com to get the key. To use this resource, you would need to first create the Link module.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NetApp::FSxN::SvmPeer",
    "Properties" : {
        "<a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>" : <i><a href="passwordsource.md">PasswordSource</a></i>,
        "<a href="#filesystemid" title="FileSystemId">FileSystemId</a>" : <i>String</i>,
        "<a href="#linkarn" title="LinkArn">LinkArn</a>" : <i>String</i>,
        "<a href="#fsxndestinationinfo" title="FsxnDestinationInfo">FsxnDestinationInfo</a>" : <i><a href="fsxndestination.md">FsxnDestination</a></i>,
        "<a href="#peersvmname" title="PeerSvmName">PeerSvmName</a>" : <i>String</i>,
        "<a href="#svm" title="SVM">SVM</a>" : <i><a href="svm.md">Svm</a></i>,
        "<a href="#applications" title="Applications">Applications</a>" : <i>[ String, ... ]</i>
    }
}
</pre>

### YAML

<pre>
Type: NetApp::FSxN::SvmPeer
Properties:
    <a href="#fsxadminpasswordsource" title="FsxAdminPasswordSource">FsxAdminPasswordSource</a>: <i><a href="passwordsource.md">PasswordSource</a></i>
    <a href="#filesystemid" title="FileSystemId">FileSystemId</a>: <i>String</i>
    <a href="#linkarn" title="LinkArn">LinkArn</a>: <i>String</i>
    <a href="#fsxndestinationinfo" title="FsxnDestinationInfo">FsxnDestinationInfo</a>: <i><a href="fsxndestination.md">FsxnDestination</a></i>
    <a href="#peersvmname" title="PeerSvmName">PeerSvmName</a>: <i>String</i>
    <a href="#svm" title="SVM">SVM</a>: <i><a href="svm.md">Svm</a></i>
    <a href="#applications" title="Applications">Applications</a>: <i>
      - String</i>
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

#### PeerSvmName

The name of the destination peer SVM.

_Required_: Yes

_Type_: String

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### SVM

_Required_: Yes

_Type_: <a href="svm.md">Svm</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Applications

A list of applications that will use the SVM peer relationship.

_Required_: Yes

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
