# Lab Infrastructure & Virtualization Setup

## Definitions

* **Hypervisor:** A hypervisor (specifically a Type 2 hypervisor like Oracle VirtualBox) is a software layer that sits on top of your host operating system. It manages the allocation of hardware resources—such as CPU, RAM, and storage—to one or more virtual environments, allowing them to run simultaneously as if they were independent physical computers.


* **Virtual Machine (VM):** A VM is a software-based emulation of a physical computer. It runs its own operating system (Ubuntu 24.04 Server) and applications. The VM is isolated from the host hardware, meaning software running inside the VM cannot natively alter the host OS files unless explicitly configured to do so.

## Why Isolation Matters

Isolation is the cornerstone of cybersecurity experimentation. By creating a sandbox, you ensure that any malicious code, faulty configurations, or catastrophic system errors are contained within the virtual disk. If the VM crashes or is compromised, the Host OS remains unaffected. 

Virtualization directly reinforces the **CIA Triad**:



* **Confidentiality:** Virtualization allows you to encrypt or wall off sensitive data from the host system, ensuring only authorized processes access the data.
* **Integrity:** Snapshots allow you to revert a VM to a "known good state," ensuring that even if a system is tampered with, you can restore its original, clean configuration.
* **Availability:** Because virtual machines are essentially files, they are portable and can be backed up or replicated instantly, ensuring you can restore your infrastructure quickly if a system fails.

### References
* Oracle. (2026). *Oracle VM VirtualBox User Manual*. Oracle Corporation. https://www.virtualbox.org/manual/
* zero two mastery. (2024). *what is a virtual machine*. https://zerotomastery.io/courses/ 
---

## Reflection

Isolation is critical when testing software or malware because it prevents the spread of unauthorized code or system instability to your primary production environment. By running experiments in a virtualized container, I can observe the behavior of potentially malicious scripts—like those used in our audit logs—without risking my actual laptop's core files. 

Virtualization supports secure experimentation by allowing for "snapshots," which act as a safety net, enabling me to test destructive commands and then reset the environment to a pristine state instantly. This practice aligns most closely with the **Cloud and Infrastructure Security** domain. Secure experimentation relies on the ability to rapidly provision and destroy environments, which is exactly how modern cloud infrastructure scales and protects assets. Ultimately, this approach turns a potentially dangerous task into a controlled, repeatable process.