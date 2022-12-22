# Renewable Energy Sites - Workday Extend

This app creates a model business object in Workday to store information about renewable energy sites. It features pages (PMDs) to view, create, and update sites. 

This app is the counterpart to the [Renewable Energy Sites](https://github.com/peter-rvb/renewable-energy-sites) app. The information on renewable energy sites is fetched by the associated React app, demonstrating how Workday Extend capabilities are brought to non-Workday systes and applications. 

Please note this project is for demonstration and educational purposes, and is not officially supported by Workday as a production-ready application.

<img width="1225" alt="manageSites pmd" src="https://user-images.githubusercontent.com/96547808/209098717-915a3113-d5e4-4a7c-83fd-8c1b645e5174.png">

### Prerequisites

- Workday Cloud Platform Developer Account & Developer Tenant ([Workday Extend](https://developer.workday.com) subscription required)

### Model Components

- **Business Object**
    - [EnergySite.businessobject](model/EnergySite.businessobject)
- **Security Domain**
    - [ManageCreateASite.securitydomain](model/ManageCreateASite.securitydomain)
    - Secures access to the business object and pages of the application
    - *Requires in-tenant configuration*
- **Business Process** 
    - [CreateEnergySite.businessprocess](model/CreateEnergySite.businessprocess)
    - Related PMDs:
        - [energySiteApprove.pmd](presentation/energySiteApprove.pmd)
        - [energySiteRevise.pmd](presentation/energySiteRevise.pmd)
        - [energySiteActionStep.pmd](presentation/energySiteActionStep.pmd)
        - [viewRequestByEventID.pmd](presentation/viewRequestByEventID.pmd)
        - [microConfirm.pmd](presentation/microConfirm.pmd)
    - Triggered whenever a new energy site is created
    - *Requires in-tenant configuration*
- **Tasks**
    - [ManageSites.task](model/ManageSites.task)
    - Task to view energy sites directly searchable in the Workday search bar
- **Reports**
    - [AllSites.report](model/AllSites.report)
    - Advanced Report to view energy site information
