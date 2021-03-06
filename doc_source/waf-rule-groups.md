# Rule Groups<a name="waf-rule-groups"></a>

A *rule group* is a reusable set of rules that you can add to a web ACL\. For more information about web ACLs, see [Managing and Using a Web Access Control List \(Web ACL\)](web-acl.md)\.

Rule groups fall into two main categories: 
+ Managed rule groups, which AWS Managed Rules and AWS Marketplace sellers create and maintain for you
+ Your own rule groups, which you create and maintain

**Differences between rule groups and web ACLs**  
Rule groups and web ACLs both contain rules, which are defined in the same manner in both places\. They are different in the following ways: 
+ You can reuse a single rule group in multiple web ACLs by adding a rule group reference statement to each web ACL\. You can't reuse a web ACL\.
+ Rule groups don't have default actions\. In a web ACL, you set a default action for each rule or rule group that you include\. Each individual rule inside a rule group or web ACL has an action defined\. 
+ You don't directly associate a rule group with an AWS resource\. To protect resources using a rule group, you use the rule group in a web ACL\. 
+ Web ACLs have a system\-defined maximum capacity of 1,500 web ACL capacity units \(WCUs\)\. Every rule group has a WCU setting that must be set at creation\. You can use this setting to calculate the additional capacity requirements that using a rule group would add to your web ACL\. 

For information about the kinds of rules that you can use in a rule group or web ACL, see [AWS WAF Rules](waf-rules.md)\.

This section describes the types of managed rule groups that are available to you and provides guidance for creating and managing your own rule groups, if you choose to do so\. 

**Topics**
+ [Managed Rule Groups](waf-managed-rule-groups.md)
+ [Managing Your Own Rule Groups](waf-user-created-rule-groups.md)
+ [Managing Rule Group Behavior in a Web ACL](waf-using-rule-groups.md)