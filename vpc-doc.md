**Topics**
+ [Creating a VPC](#Create-VPC)
+ [Creating a Subnet in Your VPC](#AddaSubnet)
+ [Associating a Secondary IPv4 CIDR Block with Your VPC](#add-ipv4-cidr)


## Creating a VPC<a name="Create-VPC"></a>

1. Open the Amazon VPC console at [https://console\.aws\.amazon\.com/vpc/](https://console.aws.amazon.com/vpc/)\.

1. In the navigation pane, choose **Your VPCs**, **Create VPC**\.

1. Specify the following VPC details as necessary and choose **Create**\. 
   + **Name tag**: Optionally provide a name for your VPC\.
   + **IPv4 CIDR block**: Specify an IPv4 CIDR block for the VPC\. We recommend that you specify a CIDR block from the private \(non\-publicly routable\) IP address ranges as specified in [RFC 1918](http://www.faqs.org/rfcs/rfc1918.html); for example, `10.0.0.0/16`, or `192.168.0.0/16`\. 
   + **IPv6 CIDR block**: Optionally associate an IPv6 CIDR block with your VPC by choosing **Amazon\-provided IPv6 CIDR block**\. If not required, select **No IPv6 CIDR Block**\.
   + **Tenancy**: Please keep **Tenancy as Default**\. 


## Creating a Subnet in Your VPC<a name="AddaSubnet"></a>

To add a new subnet to your VPC, you must specify an IPv4 CIDR block for the subnet from the range of your VPC\. You can specify the Availability Zone in which you want the subnet to reside\. You can have multiple subnets in the same Availability Zone\. 

You can optionally specify an IPv6 CIDR block for your subnet if an IPv6 CIDR block is associated with your VPC\.

**To add a subnet to your VPC using the console**

1. Open the Amazon VPC console at [https://console\.aws\.amazon\.com/vpc/](https://console.aws.amazon.com/vpc/)\.

1. In the navigation pane, choose **Subnets**, **Create subnet**\.

1. Specify the subnet details as necessary and choose **Create**\.
   + **Name tag**: Optionally provide a name for your subnet\. Doing so creates a tag with a key of `Name` and the value that you specify\.
   + **VPC**: Choose the VPC for which you're creating the subnet\.
   + **Availability Zone**: Optionally choose an Availability Zone or Local Zone in which your subnet will reside, or leave the default **No Preference** to let AWS choose an Availability Zone for you\.

     For information about the Regions that support Local Zones, see [Available Regions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-available-regions) in the *Amazon EC2 User Guide for Linux Instances*\. 
   + **IPv4 CIDR block**: Specify an IPv4 CIDR block for your subnet, for example, `10.0.1.0/24`\. For more information, see [VPC and Subnet Sizing for IPv4](VPC_Subnets.md#vpc-sizing-ipv4)\.
   + **IPv6 CIDR block**: \(Optional\) If you've associated an IPv6 CIDR block with your VPC, choose **Specify a custom IPv6 CIDR**\. Specify the hexadecimal pair value for the subnet, or leave the default value\.

## Associating a Secondary IPv4 CIDR Block with Your VPC<a name="add-ipv4-cidr"></a>

You can add another IPv4 CIDR block to your VPC\. Ensure that you have read the applicable [restrictions](VPC_Subnets.md#vpc-resize)\.

After you've associated a CIDR block, the status goes to `associating`\. The CIDR block is ready to use when it's in the `associated` state\.

**To add a CIDR block to your VPC using the console**

1. Open the Amazon VPC console at [https://console\.aws\.amazon\.com/vpc/](https://console.aws.amazon.com/vpc/)\.

1. In the navigation pane, choose **Your VPCs**\.

1. Select the VPC, and choose **Actions**, **Edit CIDRs**\.

1. Choose **Add IPv4 CIDR**, and enter the CIDR block to add; for example, `10.2.0.0/16`\. Choose the tick icon\.

1. Choose **Close**\.





