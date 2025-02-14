# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

- Costs:
VMs provide IaaS so have a lower up-front cost with no hardware purchase neccessary. They are generally more expernsive and labor intensive, as you have to maintain the infrastructure. However, they could be more cost-effective long term for larger workloads, users, and servers.
App services provide PaaS and can be expensive as you are always paying for the service plan regardless of running services or applications. However, auto-scaling and management of your allocated hardware can simplify costs.

- Scalability:
VMs can be grouped to provide scaling through Virtual Machine Scale Sets and Load Balancers, which require manual scaling or defining rules, schedules and metrics. This can be complicated while it does offer a variety of of sizes and configurations.
App services have built-in auto-scaling and vertical or horizontal scaling by changing your service plan or the number of VM instances running. They are much easier for scaling but lose on some customization.

- Availability:
VMs can be grouped to support high availability by setting up more VM instances or configuring load balancers to distribute traffic. 
App services have built-in high availability with load balancing and supports multi-region deployments.
VMs can be deployed across multiple availability zones while app services can be configured to use availability zones.

- Workflow:
VMs provide full access and control of the OS or custom software, have flexible types and sizes to choose from (for CPU, RAM, storage), and allow for cusotm images.
App services are easier to deploy without managing the infrastrcuture, so developers can focus on the code/application, and supports continuous deployment. However, there are hardware limitations and are unable to to control underlying OS.

- My Solution and Justification:
I choose to use an App service to deploy this app since it is relatively lightweight, less costly in this situation, and easily scalable. The compute resources needed are low and within App service limits as we only need to be able to log in, view articles, and add new articles with images. It will also allow me to focus more on the coding tasks instead of managing the deploymenet and infrastructure.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

If there are many more features added or the app could grow vastly in compute resource needs or storage, there would be a need to gain customization over the environment/OS, software, and hardware. If the app has more consistent workloads with increased demand, it might better to consider VMs to handle these specific configurations and costs.
