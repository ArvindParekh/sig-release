# Roadmap and Vision

## SIG Release Roadmap for 2022 and beyond

This document contains the SIG Release Roadmap for 2022 and beyond. More
detailed information can be found on the corresponding project boards.

### Primary Focus

Establish a **consumable**, **introspectable**, and **secure** supply chain for
Kubernetes. As a supply chain we understand the defining, building and
publishing of Kubernetes related artifacts.

1. **Consumable**: Improving the usability of artifacts by making their
   consumption easier. This includes being process independent of vendor,
   employer and individuals.
1. **Introspectable**: It is clear for users at which point and how Kubernetes
   artifacts are being built. This includes the documentation of all
   deliverables as well as clarifying what we do not support. All official
   release artifacts will be built by a hermetic process that is impervious to
   human interference.
1. **Secure**: The artifacts we produce are verified for their integrity. This
   applies to their functionality (we know what we deliver) as well as their
   software security (we know when CVEs occur).

### Deliverables

The following deliverables are necessary to achieve the overall goal. Within
the following listing, all deliverables are sorted by their priority and their
state.

### Work in progress (WIP)

1. **SLSA compliance in the Kubernetes Release Process (Secure)**

   Outcome: Ensure that our release process is [SLSA](https://slsa.dev)
   compliant. We also intend to participate actively in the development of the
   framework.

   Enhancement: https://github.com/kubernetes/enhancements/issues/3027

   Project board: https://github.com/orgs/kubernetes/projects/138

1. **Moving deb/rpm package builds to community infrastructure (Consumable)**

   Outcome: Automated builds of signed `deb` and `rpm` Kubernetes packages
   within community infrastructure.

   Enhancement: https://github.com/kubernetes/enhancements/issues/1731

   Project board: https://github.com/orgs/kubernetes/projects/137

1. **Signing of release artifacts (Secure)**

   Outcome: Being able to ship signed release artifacts, which includes
   container images in the first iteration as well as all artifacts following
   on.

   Enhancement: https://github.com/kubernetes/enhancements/issues/3031

### To be done (TODO)

1. **Enhance Kubernetes binary artifact management (Consumable)**

   https://github.com/kubernetes/sig-release/issues/1372

   Enhancement: _none_

   Outcome: Being able to promote files as artifacts and using this mechanism
   for Kubernetes releases.

1. **Define and collect metrics about Kubernetes releases (Introspectable)**

   https://github.com/kubernetes/sig-release/issues/1527

   Enhancement: _none_

   Outcome: Being able to measure and interpret a set of defined metrics about
   Kubernetes releases to associate actions with those.

1. **Establish Cluster API as first-class signal for upstream releases
   (Consumable)**

   Enhancement: _none_

   Outcome: Cluster API provides a CI signal for blocking release test jobs.

1. **Enhance and simplify Kubernetes version markers (Consumable)**

   Enhancement: _none_

   Outcome: Clear documentation about available version markers as well as their
   simplified automation.

### Known Risks

1. **We rely on different SIGs for our work**

   We have a need to discuss our enhancements with different SIGs to get all
   required information and drive the change. This can lead into helpful, but
   maybe not expected input and delay the deliverable.

1. **Some topics require initial research**

   We're not completely aware of all technical aspects for the changes. This
   means that there is a risk of delaying because of investing more time in
   pre-research.

1. SLSA framework is in earlier stages and changes to it can/may affect some of
   the direction of roadmap items.

### Requests to Other Teams

1. **SIG Architecture**

   For the formalization of the released platforms and input about the overall
   supply chain.

1. **SIG Cluster Lifecycle**

   To get input for making Cluster API a first-class signal for upstream releases.

1. **SIG K8s Infra**

   For general infrastructure support we rely on.

### Done Deliverables

1. **Formalize supported release platforms (Introspectable)**

   https://github.com/kubernetes/sig-release/issues/1337

   Outcome: Definition of the life cycle for currently supported Kubernetes
   artifacts and a guideline for the community about how to add new platforms.

1. **Implement a Bill of Materials (BOM) for release artifacts (Introspectable /
   Secure)**

   https://github.com/kubernetes/release/issues/1837

   Outcome: An automated formal verification of produced release artifacts for
   every future release.

1. **Create releases landing page (Consumable)**

   https://github.com/kubernetes/website/issues/20293

   Outcome: A releases page that is up to date and acts as canonical place for
   release related information, for example links to release notes and support
   timelines.

1. **Define and implement the release cadence survey (Introspectable)**

   https://github.com/kubernetes/sig-release/issues/1526

   Outcome: A regular survey evaluating the user experience of the current
   release cadence.

1. **Distribute the load of Kubernetes artifacts between vendors (Consumable)**

   Outcome: A policy and procedure for use by SIG Release to promote container
   images and release binaries to multiple registries and mirrors.

   Enhancement: https://github.com/kubernetes/enhancements/issues/3055

1. **Simplify CVE process for release management (Secure)**

   https://github.com/kubernetes/sig-release/issues/896,
   https://github.com/kubernetes/release/issues/1354

   Outcome: A documented and simple process for handling CVE information within
   Kubernetes releases.
