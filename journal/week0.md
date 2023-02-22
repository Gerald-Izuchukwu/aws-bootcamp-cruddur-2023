# Week 0 — Billing and Architecture

## Week 0 Summary

1. I succesfully created AWS account, verified it, set up MFA for the root user and also set up an IAM user and assigned some policies(permissions) to ther user incluing Billing, Cloudwatch, Budget
2. I successfully created an eventBridge rule for the health dashboard which sends a simple notification service SNS. The output was 
```
{
  "source": ["aws.health"],
  "detail-type": ["AWS Health Event"]
}
```
3. I reviewed all the pillars of the Well Archiotected Tool
4. I recreated the architectural diagram on Lucid but it wasnt fully implemented because I ran out of the free tier. The lucid link is below
5. I researched on the technical service limits of same services, an example is the SNS service which has 300 messages per second and cannot be increased
6. I am yet to open a support to request for an increase in service limit
7. I am faced with some challenged as regards creating a billing alarm and also for cloud watch


[Lucid Link](https://lucid.app/lucidchart/478da2a9-204e-48c7-b6d6-5a14e74f1f31/edit?beaconFlowId=49F68689BDA0265B&invitationId=inv_2a80c2ae-f691-4eca-977d-bd16ab11a138&page=7Y-xBxIrOGOi#)
