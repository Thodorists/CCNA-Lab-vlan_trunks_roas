Cisco Packet Tracer VLAN & Router-on-a-Stick Lab

Σκοπός:
- Εξάσκηση στη δημιουργία VLANs και trunking
- Ρύθμιση inter-VLAN routing μέσω υποδιεπαφών router

Σημεία προσοχής:
1. Όλες οι trunk ports να έχουν encapsulation dot1q.
2. Το default gateway κάθε VLAN να είναι η IP της υποδιεπαφής του router:
   - VLAN10 → 10.0.0.62
   - VLAN20 → 10.0.0.126
   - VLAN30 → 10.0.0.190
3. Έλεγχος με ping από κάθε PC προς:
   - PC του ίδιου VLAN
   - Gateway
   - PC άλλου VLAN

Εντολές ελέγχου:
- show vlan brief
- show interfaces trunk
- show ip interface brief
- ping <ip address>

Το router δρομολογεί κανονικά μεταξύ VLANs.
