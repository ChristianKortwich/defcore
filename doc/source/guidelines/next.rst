======================
OpenStack DefCore next
======================

:Status: draft
:Replaces: 2016.01
:JSON Master: http://git.openstack.org/cgit/openstack/defcore/tree/next.json

This document outlines the mandatory capabilities and designated
sections required to exist in a software installation in order to
be eligible to use marks controlled by the OpenStack Foundation.

This document was generated from the `master JSON version <next.json>`_.

Releases Covered
==============================
Applies to Kilo, Liberty, Mitaka, Newton

Platform Components
==============================
:Required: Compute, Object

:Advisory: None

:Deprecated: None

:Removed: None




Compute Component Capabilities
==============================
Required Capabilities
-----------------------
* compute-images-create (Nova)
* compute-images-delete (Nova)
* compute-images-get (Nova)
* compute-images-list (Nova)
* compute-instance-actions-get (Nova)
* compute-instance-actions-list (Nova)
* compute-keypairs-create (Nova)
* compute-quotas-get (Nova)
* compute-servers-create (Nova)
* compute-servers-delete (Nova)
* compute-servers-get (Nova)
* compute-servers-host (Nova)
* compute-servers-invalid (Nova)
* compute-servers-list (Nova)
* compute-servers-lock (Nova)
* compute-servers-name (Nova)
* compute-servers-reboot (Nova)
* compute-servers-rebuild (Nova)
* compute-servers-resize (Nova)
* compute-servers-stop (Nova)
* compute-servers-update (Nova)
* compute-servers-verify (Nova)
* compute-volume-attach (Nova)
* compute-volume-get (Nova)
* compute-volume-list (Nova)
* compute-servers-metadata-delete (Nova)
* compute-servers-metadata-get (Nova)
* compute-servers-metadata-list (Nova)
* compute-servers-metadata-set (Nova)
* compute-servers-metadata-update (Nova)
* compute-list-api-versions (Nova)
* identity-v3-api-discovery (Keystone)
* identity-v3-tokens-create (Keystone)
* images-v2-index (Nova)
* images-v2-remove (Glance)
* images-v2-update (Glance)
* images-v2-share (Glance)
* images-v2-import (Glance)
* images-v2-list (Glance)
* images-v2-delete (Glance)
* images-v2-get (Glance)
* networks-l2-CRUD (Neutron)
* networks-security-groups-CRUD (Neutron)
* volumes-v2-create-delete (Cinder)
* volumes-v2-attach-detach (Cinder)
* volumes-v2-snapshot-create-delete (Cinder)
* volumes-v2-get (Cinder)
* volumes-v2-list (Cinder)
* volumes-v2-update (Cinder)
* volumes-v2-copy-image-to-volume (Cinder)
* volumes-v2-clone (Cinder)
* volumes-v2-availability-zones (Cinder)
* volumes-v2-extensions (Cinder)
* volumes-v2-metadata (Cinder)
* volumes-v2-reserve (Cinder)
* volumes-v2-readonly (Cinder)

Advisory Capabilities
-----------------------
* networks-l3-router (Neutron)
* networks-l3-CRUD (Neutron)
* images-v2-remove (Glance)
* images-v2-update (Glance)
* images-v2-share (Glance)
* images-v2-import (Glance)
* images-v2-list (Glance)
* images-v2-delete (Glance)
* images-v2-get (Glance)
* volumes-v2-upload (Cinder)

Deprecated Capabilities
-------------------------
* compute-auth-create (Nova)
* compute-auth-get (Nova)
* compute-auth-set (Nova)

Removed Capabilities
----------------------
* identity-v2-tokens-create (Keystone)
* compute-servers-change (Nova)




Object Component Capabilities
=============================
Required Capabilities
-----------------------
* objectstore-object-copy (Swift)
* objectstore-object-create (Swift)
* objectstore-object-delete (Swift)
* objectstore-object-get (Swift)
* objectstore-object-put (Swift)
* objectstore-object-upload (Swift)
* objectstore-object-versioned (Swift)
* objectstore-temp-url-get (Swift)
* identity-v3-tokens-create (Keystone)

Advisory Capabilities
-----------------------
* objectstore-account-quotas (Swift)
* objectstore-account-list (Swift)
* objectstore-container-acl (Swift)
* objectstore-container-quotas (Swift)
* objectstore-container-create (Swift)
* objectstore-container-delete (Swift)
* objectstore-container-list (Swift)

Deprecated Capabilities
-------------------------
* objectstore-object-access (Swift)

Removed Capabilities
----------------------
* identity-v2-tokens-create (Keystone)


Designated Sections
=====================================

The following designated sections apply to the same releases as
this specification.

Required Designated Sections
----------------------------

* Cinder : Designated sections are the API implementation code
* Glance : Designated sections are the API implementation code and domain
  model.
* Keystone : Designation is outlined per API grouping. Identity (user and
  group) management APIs will not be designated. API access (with exception of
  auth) may be prohibited by policy (resulting in HTTP 403). Designated APIs
  include both v2.0 and v3 versions where applicable.
* Nova : By default, designated except scheduler, filter, drivers, API
  extensions and networking.
* Swift : Designated sections are proxy server, object server, container
  server, account server and select middleware

Advisory Designated Sections
----------------------------

* Neutron : By default, designated for all code backing required capabilities
  except plugable components such as plugins, drivers, and API extensions other
  than those listed below.

Deprecated Designated Sections
------------------------------

None

Removed Designated Sections
---------------------------

None
