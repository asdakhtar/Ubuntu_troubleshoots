# Ubuntu_troubleshoots## 

1. 🛠️ VMware VM Network Fix (Ubuntu)

**Issue**: VM had IP (`192.168.205.130`) and gateway (`192.168.205.2`), but couldn't reach internet (`Destination Host Unreachable` on ping).

**Fix**:
- On Windows host, opened `services.msc`
- Restarted:
  - `VMware NAT Service`
  - `VMware DHCP Service`
- Rebooted VM → Internet restored ✅

**Lesson**: If VM has IP but no connectivity, check host-side VMware services before changing VM settings.
