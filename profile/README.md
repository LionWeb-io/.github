# LIonWeb -- Language Engineering on the Web 

The language engineering community around [MPS](http://jetbrains.com/mps/) is working on bringing a projectional language workbench into the cloud/browser. A rough vision of how the result could look like is summarized in [this paper](http://voelter.de/data/pub/APlatformForSystemsAndBusinessModeling.pdf). As of now, several relatively independent activities (are|have been) going on, including
* ProjectIt/Freon by Jos Warmer, Anneke Kleppe (https://www.projectit.org/), a set of components and associated meta-languages geared towards creating projectional editors in the cloud/browser, 
* [MPSServer](https://github.com/Strumenta/MPSServer) by Strumenta. It is an http and websockets server that can be started from standard and headless MPS to permit interaction with MPS from outside it. It permits to read and modify models, trigger builds, get typesystem information, etc. There is also a TypeScript client library available on NPM. It is called [MPSServer-client](https://github.com/Strumenta/mpsserver-client)
* [WebEditKit](https://github.com/Strumenta/webeditkit) by Strumenta. It is a prototypal framework for defining projectional editors that can interact with MPS through MPSServer
* Modelix by itemis (https://github.com/modelix), an  open Source platform for models on the web,
* Sergej's Service APIs (Sergej) [short description, URL]
* JetBrains Projectional Web Editor (Alex) [short description, URL]
* [StarLasu](https://github.com/Strumenta/starlasu) by Strumenta. It is a set of libraries to define and work with ASTs in Kotlin, Java, Python, TypeScript. They have been used for years in production

These tools are independent and do not provide out-of-the-box interoperability. This is unfortunate because 
* None of them provides everything that's needed for an LWB in the cloud 
* Almost none of them are broken down into components that are exposed through a well-defined API and can be used independently
* Some provide similar functionality with different interfaces for the same kind of problem (M3 layer, model loading, e.g.)
* It discourages others from developing additional components
* It is hard to explain to potential users, customers, contributors, and funders why this small community is not able to coordinate

For these reasons, we have started this project here to define interfaces and protocols that allow interop between these and other, future components. To this end, this project will
* Define the logical architecture of a cloud-based LWB
* Define component roles and their dependencies
* Collect and document the APIs and protocols between these components
* Plus other artifacts that allow the development and operation of cloud-based LWBs around these interfaces

In addition, this project aims at
* Serving as a forum where discussions around all these topics can happen
* Publishing APIs only after they have been proven to work by tools, at least prototypes, (we're not the OMG :-))
* Providing minimal implementations of these interfaces to demonstrate how they can be implemented and/or used
* Invite other stakeholders after the idea has been proven workable within the current, relatively small'ish group of people and tools

This project will not 
* Provide production-quality implementations for the architectural definitions, APIs, or protocols 
* Provide a one-fits-all solution for all use cases for cloud-based LWBs 
