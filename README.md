# Enterprise Hybrid-Cloud Infrastructure & Nutanix-VMware Implementation

## 📌 Project Overview
Deployed a production-grade 3-node Hyper-Converged Infrastructure (HCI) during my internship at **Tech Data APAC**. This project demonstrates the integration of **VMware ESXi on Nutanix NX hardware**, professional networking with **Juniper switches**, and critical hardware recovery techniques.

---

## 🛠 Tech Stack
| Category | Component |
| :--- | :--- |
| **HCI Hardware** | Nutanix NX-Series Appliances |
| **Hypervisor** | VMware ESXi 7.0/8.0 (Managed via vCenter) |
| **Networking** | Juniper EX-Series Switch (Junos OS) |
| **Legacy Support**| HPE ProLiant Gen9/Gen10 Servers |
| **Modern Ops** | Kubernetes (K8s), F5 MCP, Claude AI (AIOps) |

---

## 🚀 Key Achievements

### 1. Hybrid Virtualization: VMware on Nutanix
Successfully implemented a hybrid environment by installing **VMware ESXi directly on Nutanix NX hardware**.
* **Architecture:** Leveraged Nutanix Controller VMs (CVMs) to provision robust, distributed NFS datastores for VMware hosts.
* **Management:** Unified control via vCenter Server for High Availability (HA) and vMotion.

![VMware vCenter Dashboard](vcenter.png)

### 2. Network Segmentation (Juniper Junos OS)
Designed and executed a resilient network schema on a **Juniper EX-series switch**. Used CLI `match` filters to manage specific lab traffic.

**Logical Network Schema:**
| VLAN ID | Name | Purpose |
| :--- | :--- | :--- |
| **10** | Management | ESXi Management & vMotion traffic |
| **15** | Public/Internet | Outbound traffic via TP-Link Router |
| **18** | VM_Workloads | Dedicated network for User Virtual Machines |
| **19 / 20**| vSAN_Dual | Redundant paths for high-availability storage sync |

![Juniper CLI Configuration](juniper.png)

### 3. Critical Hardware Recovery (HPE BIOS Bypass)
Handled a high-pressure hardware failure on an HPE Gen9 server involving a **Corrupted BIOS**.
* **Action:** Leveraged **HPE Smart Storage Administrator (SSA) Offline** via bootable media to bypass faulty firmware interfaces.
* **Outcome:** Successfully provisioned RAID arrays and logical drives, ensuring zero delay in the server deployment.

![HPE SSA Offline Utility](ssa.png)

### 4. Physical Infrastructure (Real-World Setup)
Performed full hardware lifecycle tasks, from physical installation to logical configuration.

| Front View (HCI Nodes) | Rear View (Juniper Switching) |
| :---: | :---: |
| ![Front View](rack-front.jpg) | ![Rear View](rack-rear.jpg) |

---

## 📩 Contact Info
* **LinkedIn:** [Insert Your Profile Link Here]
* **Email:** [Your Email Here]
