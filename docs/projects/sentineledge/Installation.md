# SentinelEdge Endpoint Security – Installation & Initial Setup Guide

## Objective

This document guides administrators through the **installation** of SentinelEdge Endpoint Security and the completion of an **initial, secure configuration**. It provides clear, step-by-step instructions to help ensure that endpoints are protected correctly from the start.

The focus is on enabling baseline protection quickly and safely, without covering advanced tuning or troubleshooting scenarios.

---

## Intended Audience

This guide is written for:

* **IT administrators** responsible for deploying endpoint security
* **Endpoint security administrators** who manage endpoint protection policies

Readers are expected to have basic system administration knowledge and access to endpoint devices and administrative credentials.

---

## Prerequisites

Before installing SentinelEdge Endpoint Security, ensure the following prerequisites are met:

### Administrative Access

* Local administrator privileges on each endpoint
* Access to the SentinelEdge management console

### Network Requirements

* Stable network connectivity during installation
* Ability for endpoints to communicate securely with the management console

### System Readiness

* Target endpoints are powered on and accessible
* Existing endpoint security software has been reviewed to avoid conflicts

---

## System Requirements

Ensure that endpoints meet the minimum system requirements before installation.

### Supported Operating Systems

* Supported desktop and server operating systems as defined by SentinelEdge documentation

### Hardware Requirements

* Sufficient available disk space for the SentinelEdge agent
* Adequate memory to allow background security monitoring

### Permissions

* Ability to install software and run background services

---

## Installation Overview

Installing SentinelEdge Endpoint Security involves the following high-level steps:

1. Accessing the SentinelEdge management console
2. Downloading the endpoint agent
3. Installing the agent on target endpoints
4. Registering endpoints with the management console

Each step is described in detail below.

---

## Step 1: Access the Management Console

1. Sign in to the SentinelEdge management console using your administrator credentials.
2. Verify that your account has permissions to deploy endpoint agents.
3. Confirm that the console is accessible from the target network.

---

## Step 2: Download the Endpoint Agent

1. In the management console, navigate to the **Endpoint Deployment** or **Agents** section.
2. Select the appropriate agent package for your operating system.
3. Download the installation package to a secure location.

Ensure that the downloaded package has not been modified and originates from a trusted source.

---

## Step 3: Install the Endpoint Agent

Perform the following steps on each target endpoint:

1. Log in to the endpoint using an administrator account.
2. Launch the SentinelEdge agent installer.
3. Follow the on-screen installation prompts.
4. Accept the license agreement when prompted.
5. Complete the installation and allow the installer to finalize setup.

During installation, the SentinelEdge agent installs required services and prepares the endpoint for protection.

---

## Step 4: Register the Endpoint

After installation:

1. The endpoint agent automatically attempts to register with the management console.
2. Verify that the endpoint appears in the console’s endpoint list.
3. Confirm that the endpoint status shows as **Active** or **Protected**.

If registration is delayed, allow a few minutes for initial communication.

---

## Initial Protection Settings

After endpoints are registered, apply baseline protection settings to ensure immediate security coverage.

### Enable Core Protection Features

Verify that the following protection features are enabled by default:

* Malware protection
* Ransomware protection
* Behavioral monitoring

These features provide essential protection without requiring advanced configuration.

---

### Apply Default Security Policy

1. Assign the default SentinelEdge security policy to newly registered endpoints.
2. Confirm that the policy is successfully applied.

Using default policies helps ensure consistent protection across all endpoints.

---

## Verification Checklist

Use the checklist below to verify a successful installation and initial setup:

* Endpoint agent is installed successfully
* Endpoint appears in the management console
* Endpoint status shows as protected
* Core protection features are enabled
* No installation errors are reported

If all items are confirmed, the endpoint is ready for use.

---

## What This Guide Does Not Cover

This installation and setup guide does not include:

* Advanced policy tuning or customization
* Performance optimization
* Troubleshooting installation or connectivity issues

These topics are addressed in separate documentation.

---

## Summary

By following this guide, administrators can install SentinelEdge Endpoint Security and apply essential protection settings quickly and confidently. Completing the initial setup ensures that endpoints are protected against common threats while maintaining a consistent security baseline across the organization.

This guide serves as the foundation for further configuration and ongoing endpoint security management.
