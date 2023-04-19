Module 4: Destroy Environment and Summary
=========================================

.. contents:: Table of Contents

Destroy Environment
###################

When your done with the lab, make sure to run the destroy scripts to delete all resources in F5 Distributed Cloud and AWS. These should be run on the jumphost terminal within the directory /home/ubuntu/f5xc-mcn-TechXchange/.

1. Return to the jumphost terminal within the xRDP session, ensuring you are in the following directory /home/ubuntu/f5xc-mcn-TechXchange/.

.. code:: bash

    # check current directory
    pwd

    # example output
    /home/ubuntu/f5xc-mcn-TechXchange/

    # if output is different, then change path
    cd /home/ubuntu/f5xc-mcn-TechXchange/

> *Note: If you closed terminal windows, you need to export the VES_P12_PASSWORD environment variable again. Otherwise Terraform will fail "Error: Creating new Volterra APIClient: Building client: Creating configuration from options: Both P12Bundle() and Cert()/Key() are empty, invalid combination".*

.. code:: bash

    # example
    export VES_P12_PASSWORD=your_certificate_password

2. Run the Terraform destroy scripts for each cloud.

.. code:: bash

     ./cloud-A-destroy.sh
     ./cloud-B-destroy.sh
     ./cloud-C-destroy.sh

Wrap-Up
#######

At this stage you should have set up a sample app environment used various multi-cloud networking features to securely network and control your app services. You also should be familiar with the telemetry and insights from the dashboards for the various MCN services. 

We hope you have a better understanding of the F5 Distributed Cloud MCN services and are now ready to implement it for your own organization. Should you have any issues or questions, please feel free to raise them via GitHub. Thank you!

Next Steps
##########

- `Home <../README.rst>`_
