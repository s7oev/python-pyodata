Vendor-specific helpers
==============

This document presents the helpers found in ``pyodata.vendor`` 

Get the service proxy client for an OData service published on SAP BTP, ABAP environment
--------------------------------------------------------------------------

Let's assume you have an ABAP environment service instance running on SAP Business Technology
Platform. You have used this instance to provide an OData service by using, for example, the
ABAP RESTful Application Programming Model. To connect to it, you need to provide several attributes 
found in the JSON service key of the instance, as well as your username and password for SAP BTP.

``pyodata.vendor.SAP`` offers a helper that takes the arguments described above, as well as an
existing ``requests.Session`` object (or another one conforming to the same API), and adds the
required token to the session object's authorization header.

The following code demonstrates using the helper.

.. code-block:: python
