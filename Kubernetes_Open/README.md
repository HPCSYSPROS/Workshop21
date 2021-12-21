# Kubernetes with Open OnDemand Using Kyverno

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5796345.svg)](https://doi.org/10.5281/zenodo.5796345)

**Authors**
* Trey Dockendorf, Ohio Supercomputing Center

**Abstract:**
Supporting Kubernetes through Open OnDemand presents many challenges with regard to safely allowing users to run applications inside Kubernetes in a similar manner to how jobs would run in an High Performance Computing batch environment. To overcome these challenges, the Ohio Supercomputer Center has utilized the Kyverno policy engine to ensure that users using Kubernetes are doing so in a safe and secure way.

The main challenge with user-submitted Kubernetes pods was ensuring that those pods are run as the UID/GID and supplemental groups belonging to that user. Additionally, there were challenges ensuring that users were authorized for the account they specified and could be charged for the resources consumed inside Kubernetes. These challenges were solved by deploying the Kyverno policy engine and implementing policies that ensure a user’s pod has certain required configurations set. Data from our local LDAP was used by the Kyverno policies to ensure not only correct UID/GID mappings but also that only active users are running pods. These changes are used to permit Kubernetes pods launched through Open OnDemand to have access to the same file systems as the HPC batch environment.

