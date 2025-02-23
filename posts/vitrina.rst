.. title: Vitrina
.. slug: vitrina
.. date: 2025-02-21 20:44:06 UTC
.. tags: projects,BDD,showcase
.. category: prose
.. link: 
.. description: Vitrina: a portfolio building kit sites for "back end" projects.
.. type: text

Vitrina is intended to be a kit for building portfolio sites for infrastructure projects. Built around a suite of functional tests, you can clone vitrina and set up a sample site, changing only the parts relevant to your work. The tests are linked to the documentation so that you can show off your work without having to become a front end developer.
Vitrina is inspired by projects like [the realworld app](https://codebase.show/projects/realworld) , the [microservices sock shop](https://microservices-demo.github.io), [Swagger Pet Shop](https://microservices-demo.github.io)

The tests are the documentation
Specification by example, BDD https://reports.cucumber.io/reports/7be2248a-ddf6-4544-8c1e-92d2dcd129db

Showcase work in context
------------------------

    - Show infrastructure: a developer could extend some aspect of the "machine"
    - Show certainty: a tester could expand the scenarios and increase understanding
    - Show results: a data scientist could transform the reports or diagrams

Software Defined Infrastructure
-------------------------------

When you have some infrastructure, how can you tell if it's doing what it's supposed to do?


In effect, Vitrina can be thought of a series of nested pipelines::

    Provision
      Run
         Test
               Datalink
                     eth0
                     wifi0
               Network
                     eth0
                     wifi0
                Transport
                     HTTP
                     HTTPS
                     SMB
                     SMTP
               Session ...
               Presentation
                    DNS ....
       Format results
              HTML
              XML
              Markdown
    ...etc


Eva's Test Hierarchy
--------------------

In order of operations, I arrange my test labs as follows:

    0) Unit (baseline expectation/exception handler validations)
    1) Smoke (see how setting it on fire goes, and report back)
    2) Integration (collectively validating aggregated feature inter-operability)
    3) Functional (user-land expressed + internal engine(s) analysis)
    4) Conformance (internally imposed by ADR, org-reqs)
    5) Compliance (external imposed by non-internal entities (SOX, PCI-DSS, HIPAA, DoD/SEC))
    6) Regression (ensuring performance hasn't traveled backwards in RC stage(s) as a last-order measure) ---




The problem space
-----------------

    - As an infra dev, you want to display your expertise and ideally, compare/contrast to show how you overcame particular challenges.
    - As a backend dev, you want to describe the activity of the infrastructure, displaying events, metrics and system status.
    - As a presenter, you want the content to appear at a consistent level of detail and a conventional layout.

The current solution
--------------------

Currently there are two ways you can show off your work:
- Participate in an open source project and display your contributions in source.
- Create a standalone project as a running instance and inform the viewer's interaction so that they understand how you have added value.

If you manage to set up a site with some examples of your work, you may have to wrap it with work that you may not know as well, and you may not be very good at.

If you're not a front end dev, then you risk giving the wrong impression when visitors are distracted by some ancient CSS, or a TLS certificate that just doesn’t behave properly.

If you're not a ops analyst, you struggle to find ways to represent activity and decide which speeds and feeds are relevant to the story you need to tell.

If you're not a network engineer, you risk creating a configuration that might not have DNS, TLS, IP, HTTP, etc. behaving as expected.

The ideal solution
------------------

Cloud computing is the result of interoperability between areas of competence so that ech component may benefit from the services of a different resource developed by folks who are good at that particular function.

The ideal solution would benefit from:
    - a collection of working components corresponding to a full stack infrastructure.
    - a checklist to validate that the components are working.
    - a reporting mechanism to display the status and activity of the project's infrastructure.
    - a high-level orchestration of the components so that you could replace an individual component and compare the results of your changes.

Sounds good, but what about implementation?
-------------------------------------------

Behaviour-driven design provides a context where you can describe desired behavior and, in the description, bind to external implementations of tests which assert that behavior.

We know that a full stack cloud infrastructure, must support a collection of services, each of which is routinely excercised during the course of most internet sessions. So we begin by asserting the existence of certain features via user journeys:

    - A browser fetches a URL
    - A DNS client resolves an address
    - A HTTP server gets a file
    - That HTTP server delivers a response.
    - The response contains HTML
    - The HTML contains text & graphics
    - The text and graphics contains test results
    - The test results enumerate the features.

Wrap it up with a bow
---------------------

  Launch a top-level script which runs the test automation and returns a list of the features and their current condition. The HTML also includes text explaining the purpose of each feature. If you decide to add, for example, high availability; then extend the tests with steps that excercise HA and edit the description to include your enhancement.

