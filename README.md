# Composable Disaggregated Infrastructure Manager

In recent years, hardware that allows for the dynamic reconfiguration of connections between servers (CPU nodes) and devices such as Memory (CXL Memory), GPUs, FPGAs, and NVMe SSDs via PCI Express/CXL switches—known as Composable Disaggregated Infrastructure (hereinafter referred to as CDI)—has begun to be released by various hardware vendors.

Composable Disaggregated Infrastructure Manager (hereinafter referred to as CDIM) is a open-source common management platform for CDI. It provides for the following features:

* Plugin mechanism that absorbs the control interface differences of CDIs for each hardware vendor.  
* Bulk configuration changes of the CDI based on the overall system design input.
* Performance monitoring of hardware resources (CPU, GPUs, etc.).

To control hardware using CDIM, a compatible plugin is required. As a reference implementation, a hardware emulator and plugin compliant with the [Developer's Interface Guide for Green Datacenter Architecture-based Computing Environment][DIG] are being provided.

## Documents

To get started with CDIM and learn the fundamentals, please refer to the following:

* Getting started
  * [English][Getting Started]
  * [Japanese][Getting Started ja]
* Tutorial
  * [English][Tutorial]
  * [Japanese][Tutorial ja]

For comprehensive information and guidance on maximizing your CDIM experience, including details on all aspects of the platform, please consult our official documentation:

* [Documents][]


## Service components

For more information about the relationship between each project/service, see Concepts.

* Concepts
  * [English][Concepts]
  * [Japanese][Concepts ja]

### Base services

| Source code repository | Compose recipe repository |
|--|--|
| Compose recipe only | [base-compose][] |

### Frontend services

| Source code repository | Compose recipe repository |
|--|--|
| [mf-core][] | Same as left |
| [mf-resource][] | Same as left |
| [mf-layout][] | Same as left |
| [mf-user][] | Same as left |
| [mf-shared-modules][] | Same as left |

### Backend services

#### Configuration management services

| Source code repository | Compose recipe repository |
|--|--|
| [configuration-manager][] | [configuration-manager-compose][] |
| [configuration-collector][] | [configuration-collector-compose][] |
| [configuration-exporter][] | [configuration-exporter-compose][] |

#### Layout apply services

| Source code repository | Compose recipe repository |
|--|--|
| [layout-apply][] | [layout-apply-compose][] |
| [migration-procedure-generator][] | [migration-procedure-generator-compose][] |

#### Performance management services

| Source code repository | Compose recipe repository |
|--|--|
| Compose recipe only | [performance-manager-compose][] |
| [performance-collector][] | [performance-collector-compose][] |
| [performance-exporter][] | [performance-exporter-compose][] |

#### Hardware control services

| Source code repository | Compose recipe repository |
|--|--|
| [hw-control][] | [hw-control-compose][] |

##### Reference hardware plugins

| Source code repository | Compose recipe repository |
|--|--|
| [fm-plugin-reference][] | - |
| [oob-plugin-reference][] | - |

### Reference hardware emulator

| Source code repository | Compose recipe repository |
|--|--|
| [hw-emulator-reference][] | [hw-emulator-reference-compose][] |

## Miscellaneous

### Installer

| Repository | Description |
|--|--|
| [installer][] | Installer for CDIM |
| [set-up-tools][] | Toolset for executing integration settings such as Kong |

### Logger library

| Repository | Description |
|--|--|
| [cdim-go-logger][] | CDIM's logger library for Go |
| [cdim-python-logger][] | CDIM's logger library for python |

## Contributing

We appreciate your interest in contributing to our project! However, please note that we are currently in the early stages of development and are not accepting external contributions at this time.

We plan to open up the contribution process in the future and will provide guidelines on how to contribute effectively once we are ready. 

Thank you for your understanding and support!

## Acknowledgments

* This software is based on results obtained from a project, JPNP21029, subsidized by the New Energy and Industrial Technology Development Organization (NEDO).

## License

[Apache License 2.0][]

<!-- Link informations  -->

[DIG]: https://unit.aist.go.jp/pprc/gdc/english/information/DIG/index.html

[Getting Started]: https://github.com/project-cdim/docs/blob/main/getting-started/en/README.md
[Getting Started ja]: https://github.com/project-cdim/docs/blob/main/getting-started/ja/README.md
[Tutorial]: https://github.com/project-cdim/docs/blob/main/tutorial/en/README.md
[Tutorial ja]: https://github.com/project-cdim/docs/blob/main/tutorial/ja/README.md
[Documents]: https://github.com/project-cdim/docs

[Concepts]: https://github.com/project-cdim/docs/blob/main/concepts/en/README.md#architecture
[Concepts ja]: https://github.com/project-cdim/docs/blob/main/concepts/ja/README.md#アーキテクチャ

[base-compose]: https://github.com/project-cdim/base-compose

[mf-core]: https://github.com/project-cdim/mf-core
[mf-resource]: https://github.com/project-cdim/mf-resource
[mf-layout]: https://github.com/project-cdim/mf-layout
[mf-user]: https://github.com/project-cdim/mf-user
[mf-shared-modules]: https://github.com/project-cdim/mf-shared-modules

[configuration-manager]: https://github.com/project-cdim/configuration-manager
[configuration-collector]: https://github.com/project-cdim/configuration-collector
[configuration-exporter]: https://github.com/project-cdim/configuration-exporter
[configuration-manager-compose]: https://github.com/project-cdim/configuration-manager-compose
[configuration-collector-compose]: https://github.com/project-cdim/configuration-collector-compose
[configuration-exporter-compose]: https://github.com/project-cdim/configuration-exporter-compose

[layout-apply]: https://github.com/project-cdim/layout-apply
[migration-procedure-generator]: https://github.com/project-cdim/migration-procedure-generator
[layout-apply-compose]: https://github.com/project-cdim/layout-apply-compose
[migration-procedure-generator-compose]: https://github.com/project-cdim/migration-procedure-generator-compose

[performance-collector]: https://github.com/project-cdim/performance-collector
[performance-exporter]: https://github.com/project-cdim/performance-exporter
[performance-manager-compose]: https://github.com/project-cdim/performance-manager-compose
[performance-collector-compose]: https://github.com/project-cdim/performance-collector-compose
[performance-exporter-compose]: https://github.com/project-cdim/performance-exporter-compose

[hw-control]: https://github.com/project-cdim/hw-control
[hw-control-compose]: https://github.com/project-cdim/hw-control-compose

[fm-plugin-reference]: https://github.com/project-cdim/fm-plugin-reference
[oob-plugin-reference]: https://github.com/project-cdim/oob-plugin-reference

[hw-emulator-reference]: https://github.com/project-cdim/hw-emulator-reference
[hw-emulator-reference-compose]: https://github.com/project-cdim/hw-emulator-reference-compose

[Installer]: https://github.com/project-cdim/installer
[set-up-tools]: https://github.com/project-cdim/set-up-tools

[cdim-go-logger]: https://github.com/project-cdim/cdim-go-logger
[cdim-python-logger]: https://github.com/project-cdim/cdim-python-logger

[Apache License 2.0]: http://www.apache.org/licenses/LICENSE-2.0
