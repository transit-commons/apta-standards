# **APTA Transit Data Standards \- GTFS Schedule Implementation Guide**

**Initial Comment Period Closes:** February 18, 2025

The goal for this document is to collect input and feedback for a paper to be published through APTA’s standards process that provides a comprehensive overview of the state of best practices for working with GTFS Schedule data at an agency. The intended audience could range from someone working at a small agency with little support or existing practice to someone starting a new role at a large agency with lots of poorly documented existing practice to a veteran GTFS maintainer who wants to make sure they’re up to date on the latest tips and tricks. The executive summary will serve as an asset for that person to take to their leadership, or an entrypoint for an executive to know who to pass the rest of the document to.

Where existing resources that we expect to stay online long-term exist, we want to reference those instead of duplicating them. After publishing the eventual document through APTA’s standards process, a living version on GitHub will accept contributions on an ongoing basis and we will periodically publish new editions through APTA.

**Please add your thoughts/notes directly into this document; we appreciate your contributions\!**

---

## **Contributing Guidelines**

Welcome to our community brainstorming document\! We encourage contributions from everyone interested in transit data standards, regardless of your level of experience. Here's how you can help:

* **Add your thoughts anywhere**: Drop in ideas, links, bullet points, or partial thoughts under any section  
* **Don't worry about polish**: Rough ideas and quick notes are valuable  
* **Share real examples**: Link to relevant projects, tools, or implementations you know about  
* **Ask questions**: Note areas that need clarification or further exploration  
* **Suggest scenarios**: Add real-world use cases that should be considered

Ways to contribute:

1. **Comment or suggest**: Access must be requested to view or contribute to this document. Feel free to invite any colleagues.  
2. **Direct editing**: Request edit access through Google Doc's "Request access" feature if you'd like to add content directly  
3. Use comments to discuss ideas with others  
4. Feel free to expand the outline with new sections or propose a better sequence

Remember: This is a collaborative brainstorming phase. All input is valuable, even if it's just a quick thought or partial idea.

---

## **Original Proposals**

* [Document: GTFS Best Practices \#1](https://github.com/transit-data-collab/documents/issues/1)  
  * Original outline proposed by John Levin  
  * Feedback from Lina  
* SWG monthly discussion on structure of documents and executive summary featuring department responsibilities/stakes

---

## **Document Outline**

* Executive Summary

  * Overview  
    * What is GTFS Schedule  
      * vs other GTFS standards  
    * Why does GTFS Schedule matter  
    * What it takes to implement GTFS Schedule

  * Key stakeholders and ownership recommendations

    * Champion/Owner:  
      * Operations/Planning Department?  
        * Primary user of schedule/service data  
        * Direct connection to service delivery  
        * Natural bridge between IT and service planning  
      * Customer Service?

    * Department Responsibilities and Stakes  
      * Operations / Planning  
        * Responsible for maintaining schedules and exporting from scheduling systems  
      * Customer Service  
        * Public-facing schedule information  
        * Responsible for ensuring quality of end-user experience consuming GTFS data  
      * Asset Management  
        * Stop/station infrastructure  
        * Accessibility information (stops & vehicles)  
      * Finance/Admin  
        * Procurement and vendor management  
      * Compliance  
        * NTD reporting requirements

* Sections

  * What systems and tools are involved

    * Transit technology component diagrams

    * Users of GTFS outside of the transit operations/customer navigation data flow

      * Policymakers/analysts on their behalf

      * Researchers  
    * Both proprietary and open-source

  * Procurement language  
    * What to ask for in procurement and why

  * Data Governance needs  
    * What aspects of data governance are important  
    * Identified data owner and data stewards for schedule data (business roles \- not IT roles)  
    * GTFS Data ownership/curation best practices for various governmental structures  
      * Small agencies who can’t maintain themselves but exist in a regional context  
      * Small agencies in rural areas  
      * Large agencies  
      * Agencies that manage or host on behalf of others (ex: one agency in a region posts feeds for multiple agencies)  
      * etc.  
    * Definition of high-quality data  
      * Data that is fit for purpose  
      * Highlight the key most common data quality dimensions relevant to GTFS  
    * Data quality monitoring  
      * Use of Data Quality Management Plans (or similar)  
      * Automated monitoring \- who does it, what standards do they follow, how to align to internal data quality practices  
      * Corrective processes for resolving issues in current dataset  
      * Preventative processes for resolving issues upstream (to prevent future issues from happening) \- includes communication with data stewards/owners \- potential root cause analysis & process change (internally or with partners/vendors)  
    * Data quality requirements / policies / mechanisms  
      * In vendor contracts  
      * In grants  
      * Incentives  
      * DQ steps built in production/maintenance processes

  * Data management needs/ challenges  
    * What are the the issues with the data  
    * What is the processing that is needed, etc.  
    * Historical archiving  
    * Manual cleaning of GTFS data published by vendor systems  
    * Managing modified schedules (ex: holidays, events, closures/changes for maintenance, openings, etc.)

  * Staffing / roles and/or consulting support  
    * What is needed to do this work  
    * Communication between stakeholders  
  * Sample project plans and steps

  * Use Cases  
    * Publishing GTFS Feed  
      * Importance of publishing to public URL endpoint  
    * Role of GTFS static in publishing GTFS-rt  
      * Importance of making sure TripIDs match between static & RT  
      * Often there are different vendors, internal product owners, and review/update timelines between GTFS static & rt \- these *must* be synced up  
    * Submitting to NTD  
    * Operational Reporting

  * Additional Resources  
    * Official resources  
      * [https://gtfs.org/](https://gtfs.org/)  
      * [https://mobilitydata.org/](https://mobilitydata.org/)	  
    * Reference implementations  
      * [https://reports.calitp.org/](https://reports.calitp.org/)  
    * Training materials  
    * Community resources  
      * [https://dot.ca.gov/cal-itp/california-transit-data-guidelines](https://dot.ca.gov/cal-itp/california-transit-data-guidelines)  
      * [https://mobilitydatabase.org/](https://mobilitydatabase.org/)  
      * [https://resources.transitapp.com/article/459-gtfs-static](https://resources.transitapp.com/article/459-gtfs-static)   
      * [Navigating the Transit Data Landscape](https://www.socallinuxexpo.org/sites/default/files/presentations/Navigating%20the%20Transit%20Data%20Landscape.pdf)  
    * Support channels  
      * MobilityData Slack

---

## **Research Tasks**

- [ ] Survey existing agency implementations  
- [ ] Document common vendor approaches  
- [ ] Collect sample procurement language  
- [ ] Compile cleaning/validation procedures  
- [ ] Gather example project plans  
- [ ] Interview agency practitioners  
- [ ] Review NTD requirements  
- [ ] Evaluate open source tools

## **Contributors**

- John Levin \- Metro Transit  
- Lina Kulikowski \- Broward County Government  
- Jeff Kessler \- Keolis Commuter Services  
- Chris Alfano \- Jarvus Innovations  
- Cassie Schmitt \- Sound Transit \- Data Governance  
-   
- \[Name\] \- \[Organization\] \- \[Role/Expertise\]

## 

## **Jeff’s Brain-Dump**

\# What is GTFS?

\#\#\# About

GTFS, or the General Transit Feed Specification, is a data standard used by transit operations around the world to describe and model their service to customers in a machine-readable format.

\#\#\# History

GTFS was first designed by several North American transit agencies in conjunction with Google in an attempt to add transit information to Google Maps. The structure of the data was built to resemble how many transit operations already structure and define their data, both in existing scheduling software and in spreadsheet formats.

\#\#\# Today

In the nearly 2 decades since conceptualization, the GTFS standard has rapidly expanded and serves as the backbone for trip planners, Mobile applications, digital signage, and most mapping platforms. operationally, this data and its importance has grown, being used as the basis for many planning and route, expansion tools, and being a required submission as part of the FTA's National Transit Database (NTD) reporting.

\#\#\# Other Components

In addition to the schedule component of GTFS, the standard has been extended multiple times to incorporate the addition of new items (like fares and pathways) and been linked to other standards, like the counterpart GTFS-Realtime (GTFS-RT) specification for real-time information.

\# Importance of Accurate GTFS

\#\#\# Why GTFS Matters

Beyond being an FTA requirement to publish this data at least once annually, using GTFS and making the data widely available ensures current customers and potential future customers have access to accurate transit information alongside mapping information already at their fingertips, eliminating a barrier to travel and promoting use of the service.

Likewise, investing in quality GFS production allows for standardized, pipelines of custom messaging and information, eliminating staff requirements for bespoke system updating and relaying information to downstream systems.

Finally, as digital mediums become more common and the preference for customers, providing accurate information in digital formats reduces the demand for such information to be provided in a printed format, often itself requiring extensive effort to produce, while also ensuring compliance with accessibility guidelines.

Having accurate GTFS data can also benefit agencies by enabling them to tap into an extensive ecosystem of tools and resources already in existence that are built upon GTFS data structure.

\#\#\# Why Regular Updates Matter

Regularly and reliably publishing updated GTFS information is critical to ensuring customers have accurate schedule information, rivaling the importance of printed schedules and supplemental schedule information provided in years past.

\# What's included in GTFS?

\#\#\# An Overview of the Standard

At its core, GTFS relies on building comma-separated text files containing the relevant information about various components of a transit operation. Among others, key files include:

\- \`agency.txt\` to provide information about the agency, it's website, and access to additional information and resources (e.g. phone number).

\- \`routes.txt\` to provide information about an agency's various routes.

\- \`stops.txt\` to provide information about designated stops that an agency may serve.

\- \`trips.txt\` to provide information about specific trips operating on each route.

\- \`stop\_times.txt\` to provide information about the places and times at which each trip will be stopping.

Countless other files and fields can also be added to enhance the quality and caliber of information reflected in the data model. For example:

\- Agencies can model large station complexes, including entrances, walkways, elevators, stairways, escalators, and other means of travel between locations within each station.

\- Agencies can model complex, fare rules and classifications for pricing available across their network.

\- Agencies can model connections across routes, stops, and trips, incorporating Block information to provide in-seat transfer opportunities, too.

By nature of being built using comma-separated text files, the GTFS standard also supports custom fields and extensions that can be used to power additional internal resources and provide other relevant information beyond that which is already incorporated in the specification. The active community surrounding GTFS, though, actively encourages development and support of the standard, adopting proposed additions to avoid reinventing the wheel over time. 

\#\#\# Getting Started with GTFS

Ultimately, GTFS data is simply a collection of text files that can be produced by anyone.

No specialized systems are required for the creation of GTFS, although many tools exist to assist in the automatic creation of the data. For example, most scheduling systems used by large transit agencies — including Hastus and Trapeze — include the ability to generate GTFS data from schedule information loaded in these systems.

For information on resources available to assist in the creation of GTFS, review the applicable items in the below "additional resources" section.

\#\#\# Sharing GTFS Data

Once the relevant GTS files have been created, a best practice is to validate this information using the canonical GTFS Validator tool. This tool provides warnings to agencies about information that may be malformed, and notes any errors contained in the GTFS that may prevent it from being loaded by various consumers.

After validation, the zipped file containing the relevant GFS files should be posted to a publicly-accessible permalink\[^1\].

In addition to posting the link, it is helpful to reach out to large tech platforms that consume this information to ensure your schedule information is added to their databases. Major players include Google Maps (via their transit partner platform), Apple Maps, Transit App, and more.

Some agencies provide a mechanism to notify consumers of when their schedule information is updated; this often takes the form of a mailing list or a subscribeable RSS feed. 

\# Best Practices

\#\#\# Build a GTFS Ecosystem

In order to truly reap the most value from GTS, agencies should focus on making GFS data the "single source of truth" for customer-facing schedule information across the organization.

This means, to the greatest extent possible, GTFS data should serve as the backbone for information posted on websites, information loaded into trip planners, information provided to customers via call centers and automated messaging, information displayed on departure displays, and a baseline of information from which alerts and real-time information is published.

Having such a pipeline, not only insure as consistent information is provided to customers across all platforms, but likewise insurers a reduction in staff time needed to provide be spoke updates to many desperate systems. Similarly, given the widespread use and adoption of GTFS data throughout the industry, most vendors support the production and consumption of GTFS data "off-the-shelf," meaning integration with existing vendors is a relatively easy feat.

\#\#\# Include Modified Schedules

In order to have a streamlined pipeline of robust information, insuring the accuracy of information from the pipeline is of the upmost importance. Therefore, while schedule information must be updated at least to incorporate changes to base schedules, republishing schedule information to account for planned service modifications — adjustments to schedules, detours, re-routes, adjustments to routes, etc. — is likewise critical.

\# Additional Resources

Countless resources are available to assist in learning about GTFS, producing GTFS, consuming GTFS, and more.

\[^1\]: A consistent link that does not change each time the file is updated.

