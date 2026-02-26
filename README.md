# Home Assistant EPEX Solutions - Node-RED Flows

🇳🇱 **Nederlands**: EPEX elektriciteitsdata voor Home Assistant via Node-RED flows met APEX-CHARTS YAML templates

🇬🇧 **English**: EPEX electricity price data for Home Assistant using Node-RED flows with APEX-CHARTS YAML templates

---

## 🎯 Overview

This repository contains **3 complete, ready-to-use solutions** for fetching EPEX electricity price data from different platforms and integrating it with Home Assistant. Each solution includes:

✅ **Node-RED Flow** (JSON export - copy & paste ready)  
✅ **JSON formatted data** (optimized for APEX-CHARTS)  
✅ **Home Assistant integration** (MQTT or Entity Sensor)  
✅ **YAML templates** (ready-to-use dashboard cards)  
✅ **Minimal configuration** (only 2-3 parameters to set)  
✅ **Complete documentation** (NL + EN)

---

## 🚀 Quick Start

### Choose Your Solution

| Solution | Platform | Best For | Link |
|----------|----------|----------|------|
| **Solution 1** | ENTSOE-E | Europe-wide data | [View](solutions/solution-1-entsoe/) |
| **Solution 2** | TenneT (NL) | Dutch market data | [View](solutions/solution-2-tennet/) |
| **Solution 3** | EPEX Spot | Real-time pricing | [View](solutions/solution-3-epex-spot/) |

### Installation (5 Minutes)

1. **Choose your preferred solution** from the table above
2. **Import the Node-RED flow** into your Node-RED instance
3. **Configure 2-3 parameters** (API key, region, update interval)
4. **Create Home Assistant sensor** (MQTT or direct entity)
5. **Add APEX-CHARTS card** using the provided YAML template

---

## 📋 Features

- 📊 **APEX-CHARTS compatible** - Beautiful, interactive charts
- 🔄 **Automatic updates** - Configurable refresh intervals
- 🌍 **Multi-region support** - NL, DE, BE, AT, CH, etc.
- 🔐 **Secure** - API keys handled safely
- 📱 **Responsive** - Works on mobile and desktop
- 🤖 **Automation ready** - Use data in Home Assistant automations
- 💾 **Persistent data** - Historical price tracking

---

## 📁 Directory Structure

```
epex-node-red-homeassistant/
├── README.md                          (this file)
├── LICENSE                            (MIT License)
├── .gitignore
├── CONTRIBUTING.md
│
├── docs/
│   ├── installation-guide.md          (General setup guide)
│   ├── configuration-guide.md         (Configuration reference)
│   ├── mqtt-vs-entity-sensor.md      (Which integration to choose)
│   └── troubleshooting.md             (Common issues & fixes)
│
├── solutions/
│   ├── solution-1-entsoe/
│   │   ├── README.md
│   │   ├── node-red-flow.json
│   │   ├── configuration.yaml
│   │   └── examples/
│   │
│   ├── solution-2-tennet/
│   │   ├── README.md
│   │   ├── node-red-flow.json
│   │   ├── configuration.yaml
│   │   └── examples/
│   │
│   └── solution-3-epex-spot/
│       ├── README.md
│       ├── node-red-flow.json
│       ├── configuration.yaml
│       └── examples/
│
├── yaml-templates/
│   ├── apex-charts-template.yaml      (Main chart template)
│   ├── mqtt-sensor-template.yaml      (MQTT sensor setup)
│   ├── entity-sensor-template.yaml    (Direct entity setup)
│   └── automation-template.yaml       (Example automations)
│
├── json-examples/
│   ├── sample-data-solution-1.json
│   ├── sample-data-solution-2.json
│   └── sample-data-solution-3.json
│
└── assets/
    ├── screenshots/
    ├── flow-diagrams/
    └── images/
```

---

## 🔧 Requirements

### Minimum
- Home Assistant (2024.1 or later)
- Node-RED (installed as add-on or standalone)
- Internet connection for API access

### Optional
- MQTT Broker (for MQTT integration, skip if using direct entity sensors)
- APEX-CHARTS custom card (for dashboard visualization)

---

## 📖 Documentation

| Document | Content |
|----------|---------|
| [Installation Guide](docs/installation-guide.md) | Step-by-step setup for Node-RED and Home Assistant |
| [Configuration Guide](docs/configuration-guide.md) | All configurable parameters explained |
| [MQTT vs Entity Sensor](docs/mqtt-vs-entity-sensor.md) | Help choosing the right integration method |
| [Troubleshooting](docs/troubleshooting.md) | Common problems and solutions |

---

## 🎨 Example Dashboard

Here's what your final result looks like:

```yaml
type: custom:apexcharts-card
header:
  title: EPEX Electricity Prices
series:
  - entity: sensor.epex_prices
    type: column
    stroke_width: 2
apex_config:
  chart:
    height: 300
  xaxis:
    type: datetime
```

---

## 🤝 Contributing

Found an issue? Have an improvement? See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📝 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

---

## 💬 Community

- 🇳🇱 Share your setup in the **Home Assistant Dutch Facebook Group**
- 📢 Discuss improvements in **GitHub Issues**
- ⭐ If you find this useful, please star the repository!

---

## 🙏 Credits

Created with ❤️ for the Home Assistant Dutch community.

Special thanks to all contributors and community members who provided feedback and improvements.

---

## 📞 Support

- **Issues**: Create a GitHub issue for bugs or feature requests
- **Questions**: Check [Troubleshooting](docs/troubleshooting.md) first
- **Discussions**: Use GitHub Discussions for general questions

---

## 🗺️ Roadmap

- [ ] Add more platform integrations
- [ ] Web dashboard preview
- [ ] YouTube setup tutorial
- [ ] HACS integration support
- [ ] Docker setup guide
- [ ] Advanced automation examples

---

**Last Updated**: 2026-02-26 15:29:39  
**Version**: 1.0.0
