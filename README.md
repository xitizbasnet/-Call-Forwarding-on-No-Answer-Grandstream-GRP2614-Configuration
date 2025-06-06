# 📞 Call Forwarding on No Answer – Grandstream GRP2614 Configuration

This guide explains how to configure **call forwarding on no answer** on a **Grandstream GRP2614 IP Phone**. The goal is to forward unanswered calls (after 4 rings) from **User 1 (Cabin 1)** to **User 2 (Reception)**.

---

## ✅ Use Case

If a call made to **User 1’s extension** is not answered after **4 rings**, it should automatically forward to **User 2 (Reception)**.

---

## 🛠 Requirements

* Grandstream GRP2614 IP Phone (already registered to a SIP server or PBX)
* Access to the local network
* Web browser (Chrome, Firefox, etc.)

---

## 📶 Step 1: Get the Phone’s IP Address

1. On the GRP2614 phone, press the **OK** button (center of the navigation pad).
2. The phone's IP address will be displayed on the screen (e.g., `192.168.1.50`).

---

## 🌐 Step 2: Access the Web Interface

1. Open a browser on a PC connected to the same network.
2. Type the phone’s IP address in the address bar:

   ```
   http://<IP_ADDRESS>
   ```

   Example:

   ```
   http://192.168.1.50
   ```

---

## 🔐 Step 3: Log In to the Web Interface

* **Username:** `admin`
* **Password:** Printed on the back of the phone (random password generated by Grandstream)

> ⚠️ Tip: Change the admin password after first login for security.

---

## ⚙️ Step 4: Configure Call Forwarding on No Answer

1. Go to the **Account** tab (e.g., `Account 1` if using the first SIP account).

2. Click on **Call Settings**.

3. Scroll down to the **Call Forwarding** section.

4. Set the following:

   | Setting               | Value                  |
   | --------------------- | ---------------------- |
   | Forward No Answer     | `ON`                   |
   | Target                | `Reception Extension`  |
   | No Answer Timeout (s) | `20` (approx. 4 rings) |
   | Forward Busy          | `OFF`                  |
   | Forward Unconditional | `OFF`                  |

5. Click **Save and Apply**.

---

## ✅ Result

Now, if **User 1** does not answer within **4 rings**, the call will be automatically forwarded to **User 2 at the Reception**.

---

## 📎 Optional Tips

* If using a **PBX (e.g., Grandstream UCM)**, forwarding can also be configured centrally.
* Always ensure that **Do Not Disturb (DND)** is **disabled** on the phone.

---
