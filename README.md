# MSAGartnerReflectionHW2
Homework 2 for CIS 4360 Microservice Architecture

The Gartner report by analyst Arun Chandrasekaran titled “Compute Evolution: VMs, Containers, Serverless - Which to Use When?” provides an interesting look into the development of abstractions at the compute layer. Through reading the article and its recommendations, I learned more about the past, present, and future of these abstractions, including virtual machines (VMs), containers, and serverless functions, as well as some important vocabulary surrounding these concepts and when it may be best to use one approach over another due to trade-offs each offers. For instance, I learned that virtual machines (which virtualize hardware capabilities and allow for multiple different operating systems to share the same server) boast better availability, manageability, and security than physical servers. As a result of these benefits, virtual machines should be used when different operating systems and version releases have to be managed/run, the host OS needs to be isolated, or you are dealing with monolithic applications with persistent data requirements. Hypervisor-based virtualization, hyperconverged and software-defined infrastructure, and public cloud infrastructure as a service (IaaS, which allows for the acquisition of self-service capacity while lessening capital expenditure) offer different ways to consume VMs. Alternatively, containers virtualize an operating system, allowing libraries and other runtime dependencies to be included in a container image in order to run an application, and can be standardized, allowing applications to run consistently in hybrid environments and throughout the software development lifecycle. According to the article, Kubernetes is the standard for scheduling and organizing containers, and the growth in the deployment of containerized apps has been furthered by various supporting OSS projects. Containers are best to use with lightweight, distributed, ephemeral applications that require rapid deployment to production, as well as when dealing with highly dynamic software environments (like agile development) and when recovery time, provisioning, and scaling are critical requirements. Serverless computing, like FaaS (which packages application code into fine-grained units known as functions in order to abstract away the runtime environment), offers a way to build and/or run services/applications without needing to manage infrastructure. This abstraction should be used when the degree of scaling is unknown and ever changing, when the ability to have fine-grain operation control of the runtime environment isn’t needed, and for batch computing tasks, event-driven services, and automating cloud operations/service integration. Ways to consume containers include container as a service (CaaS) and PaaS, where the primary method of consumption for serverless functions is in public cloud IaaS (a managed service is offered by most leading providers of public cloud). 

The report made clear in Figure 1 that where the compute evolution goes from hypervisors (VMs as scaling unit), to containers (application as scaling unit), to serverless functions/FaaS (functions as scaling unit), the abstractions and their various trade-offs will mean that each approach will continue to coexist for the foreseeable future. Virtual machines, containers, and serverless FaaS each fit best with different application architecture and have a varying level of support or complexity when it comes to different selection factors, such as Third-Party Independent Software Vender Support (high degree of support for VMs, medium support for containers, and low support for serverless FaaS) and statefulness (strong support for data integrity for VMs, medium for containers, and low for serverless FaaS), as shown in Table 3 in the article. The report concludes its discussion by addressing the future direction of containers and serverless; I learned that efforts are being made by open-source communities and commercial venders to mitigate the limits and increase production readiness of the different compute abstractions and that some emerging trends (like edge computing) can be identified for both containers and serverless.
