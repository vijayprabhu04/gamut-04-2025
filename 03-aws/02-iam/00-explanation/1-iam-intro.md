# What is IAM?

* IAM stands for `Identity and Access Management`
* IAM is an aws service which helps to securely control access to aws resources
* IAM can help in two possible ways
    - control login into your aws account 
    - delegating permissions to use the resources

# What would be your role with it?

* If you are an administrator
    - you can decide who is allowed to login in corporate aws account
    - decide what level of permissions to resources to be delegated

* If you are non administartor (assume that you joined as DevOps/SRE/Cloud/Database Engineer)
    - you might need to approach right team to gain access to aws account
    - ensure you have access to all the resources which your team is taking care of

# Root user

* Let's assume you are using an your mail ID to signing into aws account with your own defined password
* In this case your email ID is going to be considered as `root user`
* Eventually root user has complete access to all the services and resources in that account
* Also root user can create and delegate access to others when required

# AWS best practice

* AWS recommends to not use root user for everyday tasks especially with business accounts
* Instead any tasks done to be preffered from IAM users which is created