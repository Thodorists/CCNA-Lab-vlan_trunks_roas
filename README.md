# Cisco Packet Tracer Lab – VLANs & Router-on-a-Stick

## 🔧 Περιγραφή
Αυτό το lab δημιουργήθηκε στο Cisco Packet Tracer και παρουσιάζει τη βασική υλοποίηση VLANs με trunking μεταξύ δύο switches και δρομολόγηση μεταξύ VLANs μέσω Router-on-a-Stick.

Η τοπολογία αποτελείται από δύο switches (SW1, SW2), ένα router (R1), και έξι υπολογιστές χωρισμένους σε τρία VLANs.

---

## 🖧 Δίκτυο & VLANs

| VLAN | Όνομα | IP Δίκτυο | Συσκευές | Θέσεις |
|------|--------|------------|-----------|---------|
| 10 | Engineers | 10.0.0.0/26 | PC1–2-7-8 | SW1 & SW2 |
| 20 | HR | 10.0.0.64/26 | PC3–PC4 | SW1 |
| 30 | Sales | 10.0.0.128/26 | PC5–PC6 | SW2 |

---

## ⚙️ Ρυθμίσεις

### 🖥️ Router (R1)
Router-on-a-stick configuration:

```bash
interface GigabitEthernet0/0
 no shutdown
!
interface GigabitEthernet0/0.10
 encapsulation dot1Q 10
 ip address 10.0.0.62 255.255.255.192
!
interface GigabitEthernet0/0.20
 encapsulation dot1Q 20
 ip address 10.0.0.126 255.255.255.192
!
interface GigabitEthernet0/0.30
 encapsulation dot1Q 30
 ip address 10.0.0.190 255.255.255.192
