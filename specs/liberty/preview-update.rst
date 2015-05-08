..
 This work is licensed under a Creative Commons Attribution 3.0 Unported
 License.

 http://creativecommons.org/licenses/by/3.0/legalcode

..
 This template should be in ReSTructured text. The filename in the git
 repository should match the launchpad URL, for example a URL of
 https://blueprints.launchpad.net/heat/+spec/awesome-thing should be named
 awesome-thing.rst .  Please do not delete any of the sections in this
 template.  If you have nothing to say for a whole section, just write: None
 For help with syntax, see http://sphinx-doc.org/rest.html
 To test out your formatting, see http://www.tele3.cz/jbar/rest/rest.html

======================
 Preview stack update
======================

https://blueprints.launchpad.net/heat/+spec/preview-update

Similarly to how "heat stack-preview" shows the resources that would
be created during stack-create, there should be a way to show which
resources will be added, deleted, modified, or recreated during a
stack-update.

Problem description
===================

A user might have a stack running which cannot tolerate nodes going
down to be rebuilt.  Manually validating that each property changed
will not trigger an UpdateReplace is tedious and can be error-prone.
As a result, many users of Heat are wary of using stack-update.  If
users had the ability to preview the changes to live resources that
would happen as a result of a stack-update operation, it would give
them more confidence in using Heat to update their stacks.

Proposed change
===============

Here is where you cover the change you propose to make in detail. How do you
propose to solve this problem?

If this is one part of a larger effort make it clear where this piece ends. In
other words, what's the scope of this effort?

Include where in the heat tree hierarchy this will reside.

If your specification proposes any changes to the Heat REST API such
as changing parameters which can be returned or accepted, or even
the semantics of what happens when a client calls into the API, then
you should add the APIImpact flag to the commit message. Specifications with
the APIImpact flag can be found with the following query:

https://review.openstack.org/#/q/status:open+project:openstack/heat-specs+message:apiimpact,n,z

Alternatives
------------

- 

Implementation
==============

Assignee(s)
-----------

Primary assignee:
  jasondunsmore

Milestones
----------

Target Milestone for completion:
  liberty-1

Work Items
----------

- Make changes to the REST API to support stack-preview update.

- Make changes 

- Add "update" and "create" sub-commands for "heat stack-preview" in
  python-heatclient


Dependencies
============

- Include specific references to specs and/or blueprints in heat, or in other
  projects, that this one either depends on or is related to.

- Does this feature require any new library dependencies or code otherwise not
  included in OpenStack? Or does it depend on a specific version of library?
