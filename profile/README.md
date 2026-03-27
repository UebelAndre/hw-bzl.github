## Who we are

We are an open, decentralized community providing Bazel Central Registry (BCR) packages for hardware design. Independent of any specific company or institution, our community is driven by a global, distributed group of volunteers.

Moving away from the monolithic repositories of the legacy WORKSPACE era (like [rules_hdl](https://github.com/hdl/bazel_rules_hdl)), we fully embrace the modern [Bzlmod](https://bazel.build/external/overview) ecosystem. We provide modular, decoupled packages tailored for hardware design, allowing users to import exactly what they need. This significantly reduces performance and storage overhead while simplifying maintenance.

By coming together under one umbrella organization, we facilitate collaborative maintenance and mitigate the supply chain risks associated with individual user accounts. This structure prevents packages from stagnating if a single maintainer becomes unavailable, while also standardizing foundational interfaces (for example, ensuring all downstream rulesets can consume the same `verilog_library`). Ultimately, our community represents an ideal trade-off between decentralization, modularity, and unified management.

## Repo Status

| Name                                                         | Feature                                                      | Primary Maintainer      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | --------------- |
| [rules_verilog](https://github.com/hw-bzl/bazel_rules_verilog) | Provide foundational verilog/sv interfaces for Bazel rulesets (e.g., verilog_library). | [@MrAMS](https://github.com/MrAMS)          |
| [rules_vhdl](https://github.com/hw-bzl/rules_vhdl)           | Provide foundational vhdl interfaces for Bazel rulesets (e.g., vhdl_library). | [@UebelAndre](https://github.com/UebelAndre)     |
| [rules_verilator](https://github.com/hw-bzl/rules_verilator) | Bazel rules for [Verilator](https://github.com/verilator/verilator)-based Verilog/SystemVerilog simulation | [@MrAMS](https://github.com/MrAMS)          |
| [rules_vivado](https://github.com/hw-bzl/bazel_rules_vivado) | Bazel rules for Vivado FPGA tool                            | [@stridge-cruxml](https://github.com/stridge-cruxml) |
| [rules_chisel](https://github.com/hw-bzl/rules_chisel)       | Bazel rules for [Chisel](https://github.com/chipsalliance/chisel) hardware description language  | [@MrAMS](https://github.com/MrAMS)          |
| [rules_tcl](https://github.com/hw-bzl/rules_tcl)             | Bazel rules for the Tcl programming language                 | [@UebelAndre](https://github.com/UebelAndre)     |
| [rules_systemrdl](https://github.com/hw-bzl/rules_systemrdl) | Bazel rules for [SystemRDL](https://github.com/systemrdl)                                    | [@UebelAndre](https://github.com/UebelAndre)     |
| [rules_cocotb](https://github.com/hw-bzl/rules_cocotb)       | Bazel rules for Python-based chip (RTL) verification [Cocotb](https://github.com/cocotb/cocotb)                                       | [@UebelAndre](https://github.com/UebelAndre)     |


## Contribute

We are always thrilled to welcome new contributors and the packages they maintain.

- **Ownership and Maintenance:** The creator of any module automatically becomes its primary maintainer and has the final say on all decisions regarding their repository. However, to ensure the longevity of our packages, if a maintainer becomes unreachable for several months, other community members may step in to help maintain the project.

- **Transferring Existing Repositories:** If you have an existing external repository and want to move it under our community umbrella, you can easily do so using GitHub's [repository transfer](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository) feature.
  - Don't worry about broken links: All original URLs (including those for releases and older versions) will automatically redirect to the new address after the transfer.
  - Nothing will break, and your existing users will experience zero disruption.

- **Naming Conventions:** When naming a new ruleset package repository, we highly recommend using the `rules_*` format (e.g., `rules_vhdl`) instead of the older `bazel_rules_*` prefix.

- **Continuous Integration (CI):** To ensure high quality and build stability, we strongly recommend that every package incorporates a CI pipeline (e.g., [GitHub Actions](https://docs.github.com/en/actions/get-started/continuous-integration)) to automate testing and validation.
