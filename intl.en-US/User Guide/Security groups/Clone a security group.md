# Clone a security group {#concept_llj_2c1_ydb .concept}

Alibaba Cloud supports cloning a security group across regions and network types.

## Scenarios {#section_npf_td1_ydb .section}

You may need to clone a security group in the following scenarios:

-   You have created a security group, named SG1, in Region A, and you want to apply the same rules of SG1 to ECS instances in Region B.  Then you can clone SG1 to Region B without creating a new security group in Region B.
-   You have a security group in Classic network, named SG2. You want to apply the rules of SG2 to instances in a VPC. You can clone SG2  and choose VPC as the network type when configuring the cloning. Then in VPC network, you have a new security group that has same rules with SG2.
-   If you want to apply new security group rules to an ECS instance that are running an online business application, we recommend that you clone the security group as a backup before modifying the rules.  If the new security group rules are disadvantageous to the online business application, you can restore the rules completely or partly.

## Prerequisite {#section_cg4_b21_ydb .section}

If you want to change the network type of a security group from Classic to VPC, you have to [create a VPC and VSwitch](https://www.alibabacloud.com/help/faq-detail/27710.htm) in the target region first.

## Procedure {#section_pms_c21_ydb .section}

1.  Log on to the [ECS console](https://ecs.console.aliyun.com/#/home).
2.  In the Security Groups , select a region.
3.  In the left-side navigation pane, choose **Security Groups**.
4.  Find the target security group, and in the **Action** column,  click  **Clone Security Group**.
5.  In the Clone Security Group dialog box, set the new security group information:
    -   **Destination Region**: Select a region suitable for the new security group.  Not all regions are supported now.  The supported regions are displayed in the drop-down list.
    -   **Security Group Name**: Specify a new name for the new security group.
    -   **Network Type**: Select a network type suitable for the new security group.  If VPC is selected, you have to choose one VPC in the drop-down list.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/9724/4664_en-US.png)

6.  Click **OK**.

Upon successful creation, the Clone Security Group dialog box closes automatically. The new security group is displayed in the **Security Group List** You see the new security group there.

