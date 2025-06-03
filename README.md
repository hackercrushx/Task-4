# Task-4

## 🖥️ **On Windows Firewall**

### 1. **Open Windows Firewall Tool**

* Go to **Control Panel → System and Security → Windows Defender Firewall**
* Or search **“Windows Defender Firewall with Advanced Security”** in Start Menu.

---

### 2. **List Current Firewall Rules**

* Click **Inbound Rules** and **Outbound Rules** on the left pane.
* You’ll see a list of all active rules.

---

### 3. **Block Inbound Traffic on Port 23 (Telnet)**

* Click **Inbound Rules → New Rule** (on right panel).
* Select **Port → TCP → Specific local ports: 23**
* Choose **Block the connection**
* Apply to all profiles (Domain, Private, Public)
* Name the rule: `Block Telnet Port 23`

---

### 4. **Test the Rule**

* Use Telnet to test:
  In Command Prompt:

  ```bash
  telnet 127.0.0.1 23
  ```

  * If blocked, it should **not connect**.
  * (You may need to enable Telnet first via Windows Features).

---

### 5. **Remove the Test Block Rule**

* Go back to **Inbound Rules**
* Find the `Block Telnet Port 23` rule → Right-click → **Delete**

## 📝 **Documented Commands Summary**

### 🔹 Windows Firewall GUI

* Open: *Control Panel > Firewall > Advanced Settings*
* Add Rule: *Inbound Rules > New Rule > Port 23 > Block*
* Delete Rule: *Right-click the rule > Delete*


## 🧠 **How Firewalls Filter Traffic**

A **firewall** acts as a **security gatekeeper** that filters **incoming and outgoing network traffic** based on a defined set of rules.

* **Inbound filtering**: Blocks or allows traffic **entering** your system.
* **Outbound filtering**: Blocks or allows traffic **leaving** your system.
* Rules can be based on:

  * **Port numbers**
  * **IP addresses**
  * **Protocols (TCP/UDP)**
  * **Applications**

Firewalls help prevent **unauthorized access**, **remote attacks**, and **data exfiltration** by enforcing only trusted and necessary connections.
