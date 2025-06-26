# ⚙️ HPC Cluster Configuration with Ansible (SLURM)

A production-style Ansible playbook to configure an HPC cluster using SLURM workload manager.

---

## 🔧 Features

- Role-based Ansible structure
- Installs SLURM, Munge, and dependencies
- Configures head and compute nodes
- Templated `slurm.conf` for flexibility

---

## 🧱 Folder Structure

```
ansible-hpc-cluster/
├── inventories/
│   └── hosts
├── site.yml
├── roles/
│   ├── common/
│   │   └── tasks/main.yml
│   └── slurm/
│       ├── tasks/main.yml
│       └── templates/slurm.conf.j2
```

---

## 🚀 How to Run

1. Update IP addresses in `inventories/hosts`
2. Make sure all nodes are accessible via SSH
3. Run the playbook:
```bash
ansible-playbook -i inventories/hosts site.yml
```

---

## 📦 Roles

- `common`: Base system packages and Munge
- `slurm`: SLURM controller and node setup

---

## 📚 Useful Tips

- Requires Ubuntu or Debian-based system
- You can extend to support GPU nodes, multiple partitions, job submission testing

---

## 👨‍💻 Author

**Srustik**  
Senior DevOps Engineer | HPC Enthusiast  
📧 Connect on [LinkedIn](https://www.linkedin.com)

---

## 📃 License

MIT License – Use and adapt freely!