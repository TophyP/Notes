# Quick introduction

1. Pag nagdedeploy ng VM, madaming kasamang nadedeploy din (hindi lang magisa si VM)
   - VM
   - Associated disk
     - for OS
     - for hosting the data
   - VM should be part of a virtual network
   - Virtual network interface (attached sa VM)
   - Network security group (attached sa NIC)
   - Public IP address
2. Windows Server
   - Yung license, kasama na sa cost pag nagcreate
3. Windows 10
   - Dapat may license ka na bago magcreate.
4. VM cost is charged per hour.
5. When creating a VM, you might encounter an error.
   - One reason is dahil sa restrictions sa regions (sa free account)
6. Your compute service on the Azure platform
7. You can choose from different OS from WinServer to Linux

# Virtual Machine Types

- Each VM size belongs to a particular series (parang t3, t2 sa AWS)

# Temporary storage (D: drive)

- Amount depends on the instance size
- Stopping the VM on the portal performs a de-allocate action
  - Tatanggalin sa physical server ng Azure
  - Possible na magsstart ulit sa same slot or different slot na
- Shutting down / restarting via the VM will **NOT** de-allocate the VM
- Both deallocated and stopped statuses will incur partial charges for the OS disk since magkaibang resource sila

## Deallocated

- walang charge for the compute, only the VM
- mawawala yung files sa temporary storage

## Stopped

- may partial charge for the compute.
- Hindi mawawala yung files sa temporary storage

# Public IP address

- Pwede gumawa ng static IP address para hindi magpalit even if i-deallocate

## Deallocated

- magpapalit ng IP address

## Stopped

- hindi magpapalit ng ip address

## Setting the IP address to static

1. Click on the public IP address
2. Go to Networking
3. Go to NIC
4. Go to IP configs
5. Disassociate the IP from the machine
6. Set the IP address to static
7. Associate the IP address to the machine again