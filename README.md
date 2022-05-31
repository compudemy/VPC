# VPC Creation
Run the VPC Wizard
The VPC wizard automatically creates and configures most of your VPC resources for you.

To run the VPC wizard

In the left navigation pane, choose VPC Dashboard.

Choose Launch VPC Wizard.

![image](https://user-images.githubusercontent.com/103466963/171210319-f60506d5-6f3a-4044-a4cb-891688610a92.png)

Here, we have 4 options available to create a VPC.

VPC with a Single Public Subnet.
VPC with Public and Private Subnets.
VPC with Public and Private Subnets and Hardware VPN Access and
VPC with a Private Subnet Only and Hardware VPN Access.

In this article, we will see how to create a VPC with Public and Private Subnets.

To create a VPC with a Public and Private Subnet, select the second option from the left panel.

![image](https://user-images.githubusercontent.com/103466963/171211918-5aacd0b1-5df2-4a0f-b999-387ba6830572.png)

Here, you can specify the CIDR block, which means the IP range of the Public and Private Subnet. Both these networks will have different IP range . Both these subnets will be a subset of the main VPC CIDR.

![image](https://user-images.githubusercontent.com/103466963/171216949-4c1c1591-f9c6-4ad9-af25-d04e8ed483b1.png)


# Create Public and Private Subnets

Next we'll create the subnets inside our VPC that will hold our AWS resources.

Select Subnets in the left menu.

Click Create subnet and enter the following details:

VPC ID - Select the VPC you created above.

Subnet settings - Click Add new subnet three times to make four new subnet forms.

Subnet 1 of 4 - Enter the following details:

Subnet name - Enter public-subnet-1

Availability Zone - Select the first option (e.g. ap-southeast-2a)

Enter a CIDR block for each subnet that fits into your VPC CIDR block (e.g 10.0.0.0/24)

Subnet 2 of 4 - Enter the following details:

Subnet name - Enter public-subnet-2

Availability Zone - Select the second option (e.g. ap-southeast-2b). This must be in a different AZ to public-subnet-1.

Enter a CIDR block for each subnet that fits into your VPC CIDR block (e.g 10.0.1.0/24)

Subnet 3 of 4 - Enter the following details:

Subnet name - Enter private-subnet-1

Availability Zone - Select the first option (e.g. ap-southeast-2a)

Enter a CIDR block for each subnet that fits into your VPC CIDR block (e.g 10.0.2.0/24)

Subnet 4 of 4 - Enter the following details:

Subnet name - Enter private-subnet-2

Availability Zone - Select the second option (e.g. ap-southeast-2b). This must be in a different AZ to private-subnet-1.

Enter a CIDR block for each subnet that fits into your VPC CIDR block (e.g 10.0.3.0/24)

Click Create subnet

![image](https://user-images.githubusercontent.com/103466963/171225820-57cad5b5-b052-4b81-8b8c-3b3940cea649.png)

# Create Internet Gateway (IGW)

An AWS internet gateway (IGW) is used to enable internet access to and from subnets in your VPC. A subnet that routes traffic to an IGW is a public subnet, and a subnet that doesn't route traffic to an IGW is a private subnet. Routes are configured in route tables that we'll cover shortly.

Follow these steps to create an IGW and attach it to your VPC:

Select Internet Gateways in the left menu.

Click Create internet gateway and enter the following details:

Name tag - Enter a name for the internet gateway (e.g. my-internet-gateway)

Click Create internet gateway.

Select Actions -> Attach to VPC.

Select the VPC you created above and click Attach internet gateway.























