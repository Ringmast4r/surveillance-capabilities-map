# US Police Surveillance Intelligence Map

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=Ringmast4r.surveillance-capabilities-map)
![GitHub repo size](https://img.shields.io/github/repo-size/Ringmast4r/surveillance-capabilities-map)

An interactive visualization mapping police surveillance capabilities across the United States, integrating data from multiple authoritative sources.

## Live Demo

[View the Map](https://ringmast4r.github.io/surveillance-capabilities-map/surveillance-map-final.html)

## Features

- **Interactive Map**: Pan, zoom, and click on locations to explore surveillance data
- **Multi-Source Data Integration**:
  - EFF Atlas of Surveillance (14,000+ records, 2024-2025)
  - Federal Contracts & Grants from USASpending.gov (2025)
  - DoD 1033 Program military equipment transfers
  - FBI/DHS surveillance flight paths
- **Technology Filtering**: Toggle 19 surveillance technology categories
- **Search & Filter**: By city, state, agency, or vendor
- **Data Explorer**: View raw data with export to CSV
- **Flight Path Visualization**: FBI (red) and DHS (blue) aircraft tracking

## Technology Categories

| Category | Color | Examples |
|----------|-------|----------|
| Body Cameras | Blue | Axon, WatchGuard |
| License Plate Readers | Orange | Flock Safety, Vigilant |
| Facial Recognition | Pink | Clearview AI, NEC |
| Drones/UAV | Yellow | DJI, senseFly |
| Gunshot Detection | Red | ShotSpotter/SoundThinking |
| Cell Site Simulators | Purple | Stingray, Hailstorm |
| Third-party Investigative Platforms | Orange | Palantir, LexisNexis |
| Camera Registry | Light Blue | Ring, Fusus |
| Video Analytics | Light Purple | BriefCam, Verkada |
| Fusion Center | Pink | Information sharing centers |
| Real-Time Crime Centers | Pink | RTCC, command centers |
| Predictive Policing | Orange | PredPol, HunchLab |
| Social Media Monitoring | Blue | Geofeedia, Media Sonar |
| Phone Forensics | Green | Cellebrite, GrayKey |
| Night Vision/Thermal | White | FLIR, NVG equipment |
| Military Vehicles | Gray | MRAPs, armored vehicles |
| Aircraft | Light Blue | Helicopters, fixed-wing |

## Data Sources

- **[EFF Atlas of Surveillance](https://atlasofsurveillance.org/)** - Electronic Frontier Foundation's crowd-sourced database with rigorous source documentation
- **[USASpending.gov](https://www.usaspending.gov/)** - Official federal spending data for contracts and grants
- **[Washington Post 1033 Program Data](https://www.washingtonpost.com/graphics/investigations/police-equipment-acquisition/)** - FOIA-obtained military surplus transfers
- **[BuzzFeed Surveillance Planes](https://www.buzzfeednews.com/article/peteraldhous/spies-in-the-skies)** - FBI/DHS aircraft tracking data

## Project Structure

```
surveillance-capabilities-map/
├── surveillance-map-final.html  # Main application
├── atlas-of-surveillance.csv    # EFF Atlas data
├── surveillance-contracts.csv   # Federal contracts
├── surveillance-grants.csv      # Federal grants
├── wapo-1033-data.csv          # 1033 Program equipment
├── flight_paths.json           # FBI/DHS flight data
├── city_coords.json            # Geocoding database (474k+ cities)
└── *.py                        # Data processing scripts
```

## Local Development

1. Clone the repository
2. Start a local server:
   ```bash
   python -m http.server 8080
   ```
3. Open `http://localhost:8080/surveillance-map-final.html`

## Data Accuracy

- **EFF Atlas**: Rigorously documented with source citations (news articles, FOIA requests, official documents)
- **Federal Spending**: Direct from USASpending.gov (official government source)
- **1033 Program**: Washington Post FOIA requests
- **Geocoding**: 96.8% coverage with 474,000+ city coordinates

## Updates

- **2025-11-16**: Added 6 new technology categories, fixed 351 geocoding issues
- Added Third-party Investigative Platforms, Camera Registry (Ring), Video Analytics
- Improved township/borough recognition
- Added US territory support (PR, GU, VI)

## Privacy & Ethics

This project aims to increase transparency around police surveillance capabilities. All data is sourced from:
- Public records and FOIA requests
- Official government databases
- Investigative journalism
- Academic research

No personal information is collected or displayed.

## License

Data sources retain their original licenses. Code is provided for educational and research purposes.

## Contributing

Contributions welcome! Please ensure any data additions include proper source documentation.

## Acknowledgments

- Electronic Frontier Foundation for the Atlas of Surveillance
- BuzzFeed News for surveillance aircraft investigation
- Washington Post for 1033 Program analysis
- USASpending.gov for federal spending transparency
