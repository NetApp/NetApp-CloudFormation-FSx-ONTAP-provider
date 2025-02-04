# NetApp::FSxN::SvmPeer SecretSource

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#secretarn" title="SecretArn">SecretArn</a>" : <i>String</i>,
    "<a href="#secretkey" title="SecretKey">SecretKey</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#secretarn" title="SecretArn">SecretArn</a>: <i>String</i>
<a href="#secretkey" title="SecretKey">SecretKey</a>: <i>String</i>
</pre>

## Properties

#### SecretArn

The ARN of the secret stored in AWS Secrets Manager.

_Required_: Yes

_Type_: String

_Pattern_: <code>^arn:aws(-(cn|us-gov))?:secretsmanager:(([a-z]+-)+[0-9])?:([0-9]{12})?:secret:[^.]+$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SecretKey

Reference for the SecretKey. The actual password is stored in AWS Secret Manager.

_Required_: Yes

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

