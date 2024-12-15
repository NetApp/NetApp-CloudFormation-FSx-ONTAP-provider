# NetApp::FSxN::ExportPolicy Rule

Rules of the Export Policy.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#allowdevicecreation" title="AllowDeviceCreation">AllowDeviceCreation</a>" : <i>Boolean</i>,
    "<a href="#allowsuid" title="AllowSuid">AllowSuid</a>" : <i>Boolean</i>,
    "<a href="#anonymoususer" title="AnonymousUser">AnonymousUser</a>" : <i>String</i>,
    "<a href="#chownmode" title="ChownMode">ChownMode</a>" : <i>String</i>,
    "<a href="#clients" title="Clients">Clients</a>" : <i>[ <a href="rule.md">Rule</a>, ... ]</i>,
    "<a href="#index" title="Index">Index</a>" : <i>Integer</i>,
    "<a href="#ntfsunixsecurity" title="NtfsUnixSecurity">NtfsUnixSecurity</a>" : <i>String</i>,
    "<a href="#protocols" title="Protocols">Protocols</a>" : <i>[ String, ... ]</i>,
    "<a href="#rorule" title="RoRule">RoRule</a>" : <i>[ String, ... ]</i>,
    "<a href="#rwrule" title="RwRule">RwRule</a>" : <i>[ String, ... ]</i>,
    "<a href="#superuser" title="Superuser">Superuser</a>" : <i>[ String, ... ]</i>
}
</pre>

### YAML

<pre>
<a href="#allowdevicecreation" title="AllowDeviceCreation">AllowDeviceCreation</a>: <i>Boolean</i>
<a href="#allowsuid" title="AllowSuid">AllowSuid</a>: <i>Boolean</i>
<a href="#anonymoususer" title="AnonymousUser">AnonymousUser</a>: <i>String</i>
<a href="#chownmode" title="ChownMode">ChownMode</a>: <i>String</i>
<a href="#clients" title="Clients">Clients</a>: <i>
      - <a href="rule.md">Rule</a></i>
<a href="#index" title="Index">Index</a>: <i>Integer</i>
<a href="#ntfsunixsecurity" title="NtfsUnixSecurity">NtfsUnixSecurity</a>: <i>String</i>
<a href="#protocols" title="Protocols">Protocols</a>: <i>
      - String</i>
<a href="#rorule" title="RoRule">RoRule</a>: <i>
      - String</i>
<a href="#rwrule" title="RwRule">RwRule</a>: <i>
      - String</i>
<a href="#superuser" title="Superuser">Superuser</a>: <i>
      - String</i>
</pre>

## Properties

#### AllowDeviceCreation

Specifies whether or not device creation is allowed.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### AllowSuid

Specifies whether or not SetUID bits in SETATTR Op is to be honored.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### AnonymousUser

User ID To Which Anonymous Users Are Mapped.

_Required_: No

_Type_: String

_Pattern_: <code>^[a-zA-Z0-9_-]+$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ChownMode

_Required_: No

_Type_: String

_Allowed Values_: <code>restricted</code> | <code>unrestricted</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Clients

_Required_: No

_Type_: List of <a href="rule.md">Rule</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Index

The index of the export rule in the export policy.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### NtfsUnixSecurity

_Required_: No

_Type_: String

_Allowed Values_: <code>fail</code> | <code>ignore</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Protocols

Access Protocol(s) that the export rule describes.

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### RoRule

Authentication flavors that the read-only access rule governs.

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### RwRule

Authentication flavors that the read/write access rule governs.

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Superuser

Authentication flavors that the superuser security type governs

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

