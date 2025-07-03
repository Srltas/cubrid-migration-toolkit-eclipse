<p align="center">
  <img src="https://img.shields.io/badge/Java-21%2B-blue?logo=openjdk" />
  <img src="https://img.shields.io/badge/Maven-3.9%2B-blue?logo=apachemaven" />
</p>

# CUBRID Migration Toolkit Eclipse Plug-ins

> A collection of Eclipse plug-ins that lets you use the CUBRID Migration Toolkit (CMT) more conveniently within an Eclipse-based environment.

## 📂 Modules
| Name | Purpose |
|------|---------|
| **`bundle`**  | Packs third-party libraries into OSGi bundles, grouped by CMT module |
| **`p2-site`** | Collects those bundles&ensp;→&ensp;generates an installable P2 update site |

<details>
<summary><strong>Module Details</strong></summary>

| Bundle ID | Contains |
|-----------|----------|
| `com.cubrid.bundle.antlr4`           | ANTLR4 Runtime (4.13.2) |
| `com.cubrid.bundle.apache-poi-ooxml` | Apache POI-OOXML (5.4.1) |
| `com.cubrid.bundle.configuration`    | Shared third-party libs (core / UI) |
| `com.cubrid.bundle.core`             | Core-logic dependencies |
| `com.cubrid.bundle.log`              | Logging libraries |
| `com.cubrid.bundle.ui`               | UI dependencies |
</details>

---

## 🚀 Getting Started

### Prerequisites
| Requirement | Min. Version |
|-------------|--------------|
| Java        | **21** |
| Maven       | **3.9.0** |
| Internet    | Needed for dependency download |

### Build & Package
1) Clone the repository
```bash
git clone https://github.com/CUBRID/cubrid-migration-toolkit-eclipse.git
cd cubrid-migration-toolkit-eclipse
```

2) Install bundles
```bash
mvn -f bundle/pom.xml clean install
```

3) Generate P2 update site
```bash
mvn -f p2-site/pom.xml p2:site
```
When the build finishes successfully, an installable P2 update site will be available in `p2-site/target/repository`.
