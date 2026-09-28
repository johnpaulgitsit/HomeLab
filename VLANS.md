# The Plan for VLANs 👨🏾‍💻 #


| VLAN | Name          | Subnet           | Purpose                                   | Status                 |
| ---- | ------------  | ---------------- | ----------------------------------------- | ---------------------- |
| 10    | Management    | `192.168.1.0/24` | Management/network infrastructure         | Existing               |
| 20   | Servers       | 192.168.20.1/24 | AD, DNS, Windows Server, etc.             | Existing|
| 30   |Operations/Corporate| 192.168.30.1/24  | Windows 11 client devices used for Operations                | Existing          |
| 40   | IT/Admin      | 192.168.40.1/24  | For IT team and Admin level access       | Existing                   |
| 50   | Guest         | 192.168.50.1/24  | Open for public Users to connect          | In-Progress                  |
| 60   | Security      | 192.168.60.1/24  | Any kind of Security/IDS or monitoring tools                     | In-Progress                |


