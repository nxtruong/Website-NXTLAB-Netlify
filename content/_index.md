---
# Leave the homepage title empty to use the site title
title:
date: 2024-01-11
type: landing

sections:
  - block: markdown
    content:
      title:
      subtitle:
      text: |
        # Intelligent Cyber-Physical Systems (iCPS) Laboratory

        <!-- {{% callout warning %}}
        The website is being updated.
        {{% /callout %}} -->

        At the iCPS Lab, we develop _**autonomous and intelligent cyber-physical systems** using **control, optimization, machine learning / artificial intelligence, and advanced computing**_.
        An iCPS integrates tightly machine learning and AI for decision and real-time control of a CPS to achieve *high performance*, *adaptability*, *autonomy*, and *safety*.
        Our research approach integrates learning, AI, control, optimization, and computing to create methods, algorithms, and engineering solutions for iCPS.

        Our research is both _**fundamental**_ and _**applied**_.  The bedrock of our research is a *fundamental research thrust* that advances the theoretical and algorithmic foundation of learning and control of iCPS.  Our *practical research thrusts* focus on developing smart and autonomous systems in various application domains and on building cyberinstructures for iCPS.
        
        The iCPS Lab is in the [Department of Electrical and Computer Engineering](https://www.ece.ucf.edu/), [College of Engineering and Computer Science](https://www.cecs.ucf.edu/) at the [University of Central Florida](https://www.ucf.edu/) (UCF).
        We are also affiliated with the [School of Modeling, Simulation, and Training](https://www.cecs.ucf.edu/smst/) and the [Department of Computer Science](https://www.cs.ucf.edu/).

        <!-- [**Learn more about our research**](research) or [**join our lab**](#join) -->

        <!-- [Current opportunities](/opportunities) -->

    design:
      columns: '1'
      spacing:
        padding: ['20px', '0', '20px', '0']
  - block: collection
    content:
      title: Latest News
      subtitle:
      text:
      count: 3
      filters:
        author: ''
        category: 'news'
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
      archive:
        enable: true
        text: View All News
        link: news/
    design:
      view: compact
      columns: '1'
  - block: contact
    id: contact
    content:
      # Automatically link email and phone or display as text?
      autolink: true

      # Contact details (edit or remove options as required)
      email: truong.nghiem@ucf.edu
      address:
        street: BYC-CMMS 109, 12701 Scholarship Dr
        city: Orlando
        region: FL
        postcode: '32816'
        country: United States
        country_code: US
      coordinates:
        latitude: '28.5948'
        longitude: '-81.2024'
      directions: Enter Barbara Ying Center - CMMS (Building 81), go to room 109
      # appointment_url: 'https://calendly.com'
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'

---
