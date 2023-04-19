Lab 1: Deploy Terraform Resources in Cloud A
============================================

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

2. Deploy the Terraform code for "Cloud A" by running the script **./cloud-A-setup.sh**.

.. code:: bash

    ./cloud-A-setup.sh

3. Open F5 Distributed Cloud Console and navigate to the **Multi-Cloud Network Connect** tab.

.. figure:: ../assets/xc/cloud_a_sites.png

4. Open **Site List** and check the **Health Score**. It may take some time to provision the node.

.. figure:: ../assets/xc/cloud_a_ready.png
