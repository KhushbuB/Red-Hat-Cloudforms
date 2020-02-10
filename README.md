[Red Hat CloudForms](https://access.redhat.com/products/red-hat-cloudforms) is a one platform for multiple providers to be integrated at one single point. Different Cloud, Infrastructure, Container providers can be added to Red Hat CloudForms. Red Hat CloudForms is a Red Hat managed product for an upstream [ManageIQ](https://www.manageiq.org/) community version with Ivanchuk 5.0 as the latest release.

CloudForms Management Engine [ CFME ] is a set of packages shipped in the product. CFME is like any other machine `evmserverd` service running on the appliance. The default credentials for the appliance to login at the webUI is admin|smartvm.

Below we shall try to integrate Red Hat Virtualization as a Infrastructure provider to the environment and try creating new virtual machines in the newly integrated provider.

## Add a Cloud Provider
- Login to the Red Hat CloudForms UI
- Navigate to *Compute -> Infrastructure -> Providers*
- Go to *Configuration -> Add a New Infrastructure Provider*
- Fill in the name for the provider and choose the type as **Red Hat Virtualization**
- In the Default Endpoints tab, fill in the Hostname, Username and Password for the provider
- Validate the provider and save the fields

You can see the Provider thumbnail with the specified name at **Infrastructure Providers** dashboard.

![Add Provider](https://raw.githubusercontent.com/KhushbuB/Red-Hat-Cloudforms/master/Provider.png "Add Provider")

## Create Instances to the Cloud Provider
- Login to the Red Hat CloudForms UI
- Navigate to *Compute -> Infrastructure -> Virtual Machines*
- Go to *Lifecycle -> Provision VMs*
- Select the template to provision the Virtual Machine and continue ahead
- Fill in all the details to provision VM by selecting the Environment, Hardware and Network
- You can either create the VM immediately or you can also Schedule the VM for a particular time
- Submit the request and you see the request status at *Services -> Request*

Once the Requets status is *Finished*, you can see the Instance thumbnail with the specified name at **All VMs and Templates** dashboard.

![Instance](https://raw.githubusercontent.com/KhushbuB/Red-Hat-Cloudforms/master/Instance.png "Instance Created")
