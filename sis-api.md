---
layout: default
title: Project SIS API
nav_order: 6
---

# Project SIS API
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction

On this page, we will document information that we have regarding the SIS API that is available.  If you find an interesting command or way of using the API, please post on Piazza so we can add it to this working document.

## Basics

The SIS API is a RESTful web API that returns a JSON object based upon parameters passed to the URL.  Projects will need to dynamically build URLs as needed to request appropriate JSON objects that can then be parsed by the project.  One way to do this would be to use the `requests` and `json` libraries built into Python to make web calls.  There are numerous tutorials available on the web to help you with this.  There are also other third-party packages you could import, but these are not necessarily something we can offer any support for.

## Common Query URLs

### Finding All Department Mnemonics

`https://sisuva.admin.virginia.edu/psc/ihprd/UVSS/SA/s/WEBLIB_HCX_CM.H_CLASS_SEARCH.FieldFormula.IScript_ClassSearchOptions?institution=UVA01&term=1228`

_Replace 1228 with the appropriate term.  The formula is "1" + [2 digit year] + [12 for Spring, 8 for Fall].  So, 1228 is Fall 2022._

### Finding All Courses from a Department

`https://sisuva.admin.virginia.edu/psc/ihprd/UVSS/SA/s/WEBLIB_HCX_CM.H_CLASS_SEARCH.FieldFormula.IScript_ClassSearch?institution=UVA01&term=1228&subject=CS&page=1`

_Replace 1228 with the appropriate term. The formula is "1" + [2 digit year] + [12 for Spring, 8 for Fall].  So, 1228 is Fall 2022.  Replace CS with the desired subject.  Note that many departments with lots of classes will have multiple pages and you will have to go through all of them._

### Finding All Courses by Instructor

`https://sisuva.admin.virginia.edu/psc/ihprd/UVSS/SA/s/WEBLIB_HCX_CM.H_CLASS_SEARCH.FieldFormula.IScript_ClassSearch?institution=UVA01&term=1228&page=1&instructor_name=Horton`

_Replace 1228 with the appropriate term. The formula is "1" + [2 digit year] + [12 for Spring, 8 for Fall].  So, 1228 is Fall 2022.  Replace Horton with another name._

## Build Your Own URL

### Base URL

`https://sisuva.admin.virginia.edu/psc/ihprd/UVSS/SA/s/WEBLIB_HCX_CM.H_CLASS_SEARCH.FieldFormula.IScript_ClassSearch?institution=UVA01`

### Flags

As you can see from the examples above, you can add on additional flags using the format `&flag_name=search_value`.

* term=
* date_from=
* date_thru=
* subject=
* subject_like=
* catalog_nbr=
* time_range=
* days=
* campus=
* location=
* x_acad_career=
* acad_group=
* rqmnt_designtn=
* instruction_mode=
* keyword=
* class_nbr=
* acad_org=
* enrl_stat=
* crse_attr=
* crse_attr_value=
* instructor_name=
* session_code=
* units=
* page=1

For examples of the data, here is the URL to get Prof. Horton's 2:00 section of CS 3240: [https://sisuva.admin.virginia.edu/psc/ihprd/UVSS/SA/s/WEBLIB_HCX_CM.H_CLASS_SEARCH.FieldFormula.IScript_ClassSearch?institution=UVA01&term=1232&page=1&instructor_name=Horton&class_nbr=16031](https://sisuva.admin.virginia.edu/psc/ihprd/UVSS/SA/s/WEBLIB_HCX_CM.H_CLASS_SEARCH.FieldFormula.IScript_ClassSearch?institution=UVA01&term=1232&page=1&instructor_name=Horton&class_nbr=16031)