# A Network-Constrained Conditional Randomization Analysis of Vehicle Collisions in Philadelphia, 2020–2024

An interactive, scroll-driven **[data story](https://cyber-hbliu.github.io/Urban-Street-Networks-and-Interactive-Web-Maps/).** built with D3.js, presenting a street-network analysis of five years of [Philadelphia crash data (2020-2024)](https://data-phl.opendata.arcgis.com/datasets/21154a8f1894449f839d2288726e9837_0/explore). Every number on the site is taken directly from the accompanying paper and its verified analysis pipeline. Nothing is synthetic.


## What the analysis found

Between 2020 and 2024, Philadelphia recorded 36,303 traffic crashes. 620 were fatal, killing 647 people. Crashes fell 30% from the 2021 peak of 8,458 to 5,920 in 2024, while fatal crashes held at 143, 118, 120, 120, and 119. The fatality rate per crash rose from 1.8% to 2.0%. Crashes declined and fatalities did not.

The paper asks one question. **Do the locations of fatal crashes carry information beyond the locations of crashes in general? **The test is conditional randomization. Each of 999 draws relabels 620 of the 36,303 crashes as fatal, stratified by year so annual fatal totals and all crash locations are preserved, generating the null distribution of any spatial statistic.

**Three of four statistics come back at chance.**

- Fatal crashes fall on low-crash streets at the expected rate (25.0% observed against a null of 27.0%, p = 0.28). Quiet streets are neither hidden hazards nor protected.
- Crash and fatal hotspot sets overlap no more than random labeling produces (Jaccard 0.11 against 0.13, p = 0.35).
- A crash-volume ranking captures fatal crashes in proportion to crashes and no better. The top 12% of network length carries 71.8% of crashes and 73.9% of fatal crashes.

**Two statistics deviate, both slightly.**

- Fatal crashes occupy 2.40% of network length against a null of 2.05% (p ≤ 0.001). They spread across more distinct segments than chance predicts.
- Fatal segments repeat year over year at 5.3% against a null of 1.8% (p ≤ 0.001). A small persistent set exists. 19 of every 20 fatal segments do not repeat.

Where location is nearly uninformative, street type is not. Trunk roads record 25.0 fatal crashes per 1,000 crashes and residential streets 10.3. Arterials carry 47% of crashes and 65% of fatal crashes. The mechanism is impact speed (Tefft, 2013). The policy reading is that reactive site targeting cannot work, corridor investment is justified where the repeat-rate statistic points (Roosevelt Boulevard's speed cameras preceded a 21% drop in fatal and serious-injury crashes), and the reliable, changeable predictor is street type.

## Data

- PennDOT crash records, Philadelphia County, 2020–2024, via OpenDataPhilly. OpenStreetMap drivable network via OSMnx, projected to EPSG 2272. 
- City of Philadelphia, Vision Zero Action Plan 2030 and High Injury Network (2025). 
- Roosevelt Boulevard figures, Philadelphia Parking Authority. 
- Basemap tiles © OpenStreetMap contributors © CARTO.

## Reference

Tefft, B. C. (2013). Impact speed and a pedestrian's risk of severe injury or death. *Accident Analysis & Prevention, 50*, 871–878. https://doi.org/10.1016/j.aap.2012.07.022

## Origins

This project began as a graduate course exercise (Urban Street Networks and Interactive Web Maps, 2022) that computed a crash index for Center City using 2021 data, osmnx, and a Folium map. This repository extends that method citywide and across five years, adds the KSI and fatal indexes, network-constrained hotspot statistics with false-discovery correction, and a year-stratified conditional randomization test that turns the map into an inference problem. The pipeline runs on open data and is built to re-run each year.

[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-9f69c29eadd1a2efcce9672406de9a39573de1bdf5953fef360cfc2c3f7d7205.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=9279250)

https://classroom.github.com/a/x9a--7nH
