# Namespace as a service / Workspace as a service

Namespace as a service (NaaS) and Workspace as a service (WaaS), Both can help in providing a smooth developer experience focusing on reducing productivity lead time and standardizing/automating the developer onboarding experience.
### [Note]
Developer Experience (DX) refers to the experience of developers as they work with a company's tools, platforms, and technologies to build software applications.

### We need the following operators 
- DevWorkspace operator
- OpenShift DevSpaces operator 
- OpenShift pipelines operator 
- Namespace configuration operator

###  The demo use case covers the following scenario:
```bash
.
├── A new developer is joining the team.
├── With the first log-in a new namespace is created with the following.
│   ├── Standard name <USER>-devspaces.
│   ├── Quota and limits.
│   ├── RBAC granting the pipeline service account in team CICD namespace ‘admin’ access to the developer <USER>-devspaces.
│   ├── Add an onboarding workspace containing all the onboarding documentation required by the new developer.
│   └── Force the onboarding workspace to be running all the time.
├── Developers can not
│   ├── delete the namespace
│   └── delete or stop the onboarding-workspace
├── Developer request to access a NodeJS workspace to start NodeJS+MongoDB development
└── Platform team runs the WaaS pipeline that creates the NodeJS workspace in the developer namespace <USER>-devspaces
```

### Objects used 
- NamespaceConfig from Namespace configuration operator
- DevWorkspaceTemplate and DevWorkspace from DevSpaces operator
- Pipeline from OCP pipelines operator

### Demo 
https://lnkd.in/eiC9kXWc
