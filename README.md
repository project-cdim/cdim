# Composable Disaggregated Infrastructure Manager

In recent years, hardware vendors have started releasing hardware capable of dynamically reconfiguring connections between servers (CPU nodes) and devices such as CXL Memory, GPUs, FPGAs, and NVMe SSDs via PCI Express/CXL switches, known collectively as Composable Disaggregated Infrastructure (CDI).

Composable Disaggregated Infrastructure Manager (CDIM) is an open-source management platform specifically for CDI. CDIM offers these features:

* A plugin mechanism to handle differences in the control interfaces among various hardware vendors.
* Bulk configuration changes based on comprehensive system design inputs.
* Performance monitoring for hardware resources like CPUs and GPUs.

To utilize CDIM for hardware control, a compatible plugin is necessary. As a reference, we provide [hw-emulator-reference][], [fm-plugin-reference][] and [oob-plugin-reference][] compliant with the [Developer's Interface Guide for Green Datacenter Architecture-based Computing Environment][DIG].

## Documents

To begin using CDIM and understand its fundamentals, refer to the following documents:

* **Getting Started**
  * [English][Getting Started]
  * [Japanese][Getting Started ja]
* **Tutorial**
  * [English][Tutorial]
  * [Japanese][Tutorial ja]

For complete information on utilizing CDIM effectively, consult our full documentation:

* [Documents][]

## Service Components

For details on how each project/service interrelates, see the Concepts section:

* **Concepts**
  * [English][Concepts]
  * [Japanese][Concepts ja]

### Base Services

| Source Code Repository | Compose Recipe Repository |
|-----------------------|--------------------------|
| Compose recipe only   | [base-compose][]         |

### Frontend Services

| Source Code Repository | Compose Recipe Repository |
|------------------------|--------------------------|
| [mf-core][]            | Same as left             |
| [mf-resource][]        | Same as left             |
| [mf-layout][]          | Same as left             |
| [mf-user][]            | Same as left             |
| [mf-shared-modules][]  | Same as left             |

### Backend Services

#### Configuration Management Services

| Source Code Repository    | Compose Recipe Repository            |
|---------------------------|-------------------------------------|
| [configuration-manager][] | [configuration-manager-compose][]    |
| [configuration-collector][] | [configuration-collector-compose][] |
| [configuration-exporter][] | [configuration-exporter-compose][]   |

#### Layout Apply Services

| Source Code Repository         | Compose Recipe Repository                   |
|--------------------------------|--------------------------------------------|
| [layout-apply][]               | [layout-apply-compose][]                    |
| [migration-procedure-generator][] | [migration-procedure-generator-compose][]  |

#### Performance Management Services

| Source Code Repository       | Compose Recipe Repository                 |
|------------------------------|------------------------------------------|
| Compose recipe only          | [performance-manager-compose][]           |
| [performance-collector][]    | [performance-collector-compose][]         |
| [performance-exporter][]     | [performance-exporter-compose][]          |

#### Hardware Control Services

| Source Code Repository | Compose Recipe Repository |
|------------------------|---------------------------|
| [hw-control][]         | [hw-control-compose][]    |

##### Reference Hardware Plugins

| Source Code Repository    | Compose Recipe Repository |
|---------------------------|---------------------------|
| [fm-plugin-reference][]   | -                         |
| [oob-plugin-reference][]  | -                         |

### Reference Hardware Emulator

| Source Code Repository       | Compose Recipe Repository             |
|------------------------------|---------------------------------------|
| [hw-emulator-reference][]    | [hw-emulator-reference-compose][]     |

## Miscellaneous

### Installer

| Repository    | Description                                         |
|---------------|-----------------------------------------------------|
| [installer][] | CDIM Installer                                      |
| [set-up-tools][] | Tools for integration settings such as Kong       |

### Logger Library

| Repository          | Description                               |
|---------------------|-------------------------------------------|
| [cdim-go-logger][]  | CDIM's logger library for Go              |
| [cdim-python-logger][] | CDIM's logger library for Python        |

## Contributing

Thank you for your interest in contributing to our project! We're currently in the early stages of development, and therefore, we are not accepting external contributions at this time.

We look forward to opening up our contribution process in the future. Once we are ready, we will provide detailed guidelines on how you can contribute effectively.

We appreciate your understanding and support!

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
