# Introduction to NetScaler Programmability
This repository are the resources and code samples to accompany a short lab on NetScaler Programmability I created for a group of Cisco engineers.  

## Agenda
The following basic topics will be covered within the lab.  

* NetScaler REST API
* NetScaler and Ansible

## Resources and Further Information
### Infrastructure
This lab was built and leverages an instance of a VPX Loadbalancer hosted on AWS using the offering from the [Marketplace](https://aws.amazon.com/marketplace/pp/B00A9ZLKFK?qid=1511300917372&sr=0-8&ref_=srh_res_product_title).  

### Official Documentation
* [REST API Guide](https://docs.citrix.com/en-us/netscaler/12/nitro-api/nitro-rest.html)
* [Ansible Modules](http://docs.ansible.com/ansible/latest/list_of_network_modules.html#netscaler)
* [Nitro Python SDK](https://www.citrix.com/downloads/netscaler-adc/sdks/netscaler-sdk-release-110.html)

# Local Workstation Setup

## "Gitting" the Code
All of the code and examples for this lesson is located in the `hpreston/lab_netscaler` directory.  Clone and access it with the following commands:

```bash
git clone https://github.com/hpreston/lab_netscaler
cd lab_netscaler
```

## Local Workstation Setup
Be sure to complete the [General Workstation Setup](https://github.com/CiscoDevNet/netprog_basics/blob/master/readme_resources/workstation_setup.md) instructions before beginning this lesson.  

***Windows Support Note***
Due to Windows not currently being supported as a Control Station for Ansible, the Ansible portions of this lab require a Linux or OS X based workstation.  If you are on a Windows workstation, you'll need to have another environment for this lab.  

### Python Environment Setup
It is recommended that this lesson be completed using Python 2.7.   

It is highly recommended to leverage Python Virtual Environments for completing exercises in this course.  

Follow these steps to create and activate a venv.  

```bash
# OS X or Linux
virtualenv venv --python=python2.7
source venv/bin/activate
```

```bash
# Windows (Explicitly Provide Path to Python2.7 installation)
virtualenv venv --python=c:\Python27\python.exe
venv/Scripts/activate
```

#### Install Python Requirements for Lesson
With the Virtual Environment activated, use pip to install the necessary requirements.  

```bash
# From the code directory for this lesson
pip install -r requirements.txt
```

#### Install Python Nitro SDK from Citrix
Follow these instructions to download and install the Nitro SDK into your virtual environment.  

1. Download the [SDK from Citrix](https://www.citrix.com/downloads/netscaler-adc/sdks/netscaler-sdk-release-110.html)
2. Unzip the downloaded file, and then unzip the `nitro-python.tgz` contained within it.  (The downloaded file includes multiple SDKs for other languages)
3. Be sure to have activated the Python Virtual Environment for this lab.
4. Install the Nitro SDK

  ```bash
  python setup.py install
  ```
