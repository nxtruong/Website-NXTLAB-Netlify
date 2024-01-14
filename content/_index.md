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
        # Intelligent Control Systems (ICONS) Laboratory

        {{% callout warning %}}
        The website is being updated.
        {{% /callout %}}

        At the ICONS Lab, we develop the **learning and control foundation of intelligent cyber-physical systems**, with applications in autonomous systems.
        <!-- we develop theory, algorithms, tools, technologies, and applications of *intelligent and high-performance control systems*. -->
        <!-- These systems are at the core of many complex and critical engineering systems. -->
        An *intelligent cyber-physical system* (iCPS) integrates deeply machine learning (ML) and artificial intelligence (AI) for decision and real-time control of a CPS to achieve *high performance*, *adaptability*, *autonomy*, and *safety*.
        By integrating learning, AI, control, and optimization, we create methods, algorithms, and engineering solutions for autonomous learning and real-time operation of iCPS.
        Our research and research approaches are multi-disciplinary, combining theories and techniques from
        - *Computer science*: machine learning, AI, scientific computing;
        - *Electrical and computer engineering*: control theory, edge computing, internet-of-things (IoT), sensors, embedded systems;
        - *Applied mathematics*: optimization theory, dynamical systems;
        - and various application domains.

        We are particularly interested in the following application areas:
        - **AI-enabled smart and sustainable energy systems** such as smart buildings, connected communities, smart grids, smart cities.
        - **Smart environment sensing and monitoring systems** such as mobile robotic sensor networks (MRSN), wireless sensor networks, IoT sensing and monitoring in the built environments.
        - **Data-driven control and optimization**.

        <!-- - **Learning-based intelligent control systems** that combine machine learning (and AI), computing, optimization, and control theory.  Applications are in energy systems (particularly smart buildings and connected communities), multi-agent systems (e.g., mobile sensing networks), and transportation (e.g., advanced driver-assistance systems, self-driving cars, autonomous drones). -->

        The ICONS Lab is in the [School of Informatics, Computing, and Cyber Systems](https://nau.edu/siccs) at [Northern Arizona University](https://nau.edu/).

        [**Explore our research**](research) or [**join our lab**](#join)

        [Current opportunities](/opportunities)

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
      email: truong.nghiem@nau.edu
      address:
        street: 1295 S. Knoles Dr.
        city: Flagstaff
        region: AZ
        postcode: '86011'
        country: United States
        country_code: US
      coordinates:
        latitude: '35.1862'
        longitude: '-111.6583'
      directions: Enter Building 90 (SICCS), go straight then turn left just before the elevator
      # appointment_url: 'https://calendly.com'
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
---
