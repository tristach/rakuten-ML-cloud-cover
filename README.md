# Rakuten-ML-Cloud-Cover
A semi-automated threat detection tool which combines advanced KQL queries and Sentinel logic into a machine-readable JIT detection/warning system.
## Project Summary
Cloud-Cover automates collection and analysis of failed login attempts using:
- Microsoft Sentinel KQL queries
- Azure Logic Apps for export and notification
- Python (pandas, matplotlib) for analysis + visualization

## Process Overview
1. Deployed honeynet VMs (Windows + Linux) in Azure.
2. Configured Sentinel rules + Logic Apps to export CSV data.
3. Collected failed login attempts over 24 hours (time period adjustable) through logic app.
4. Logic app sends email with attache file (CVS) to be downloaded and moved via bash and or cut/paste (again, this version is semi-automated).
5. Used pandas to clean + group data (e.g., by AttackerIP).
6. Generated bar charts of top attacker IPs.
7. Generates real-time, useful information making playbook and or response time easier/faster.

## Example Output
![Top 20 IPs](link-to-your-image)

![image](https://github.com/user-attachments/assets/6f78c67e-6e27-455f-ae95-35b6defc27ad)
<img width="504" alt="image" src="https://github.com/user-attachments/assets/44d94401-bfef-4116-a544-410cf0664429" />
