# NetApp::FSxN::ClusterPeer ClusterPeerInfo

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#name" title="Name">Name</a>" : <i>String</i>,
    "<a href="#remoteipaddresses" title="RemoteIpAddresses">RemoteIpAddresses</a>" : <i>[ String, ... ]</i>,
    "<a href="#ipspace" title="IpSpace">IpSpace</a>" : <i>String</i>,
    "<a href="#statusinfo" title="StatusInfo">StatusInfo</a>" : <i><a href="clusterpeerstatus.md">ClusterPeerStatus</a></i>
}
</pre>

### YAML

<pre>
<a href="#name" title="Name">Name</a>: <i>String</i>
<a href="#remoteipaddresses" title="RemoteIpAddresses">RemoteIpAddresses</a>: <i>
      - String</i>
<a href="#ipspace" title="IpSpace">IpSpace</a>: <i>String</i>
<a href="#statusinfo" title="StatusInfo">StatusInfo</a>: <i><a href="clusterpeerstatus.md">ClusterPeerStatus</a></i>
</pre>

## Properties

#### Name

Optional name for the cluster peer relationship. By default, it is the name of the remote cluster.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### RemoteIpAddresses

Addresses of the remote peers. Assumes existing intercluster LIFs of remote cluster if not provided.

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### IpSpace

IPspace name of the local intercluster LIFs. Assumes Default IPspace if not provided.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### StatusInfo

_Required_: No

_Type_: <a href="clusterpeerstatus.md">ClusterPeerStatus</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

