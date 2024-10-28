# Azure Policy: Restrict Deployment Types for Azure OpenAI

This repository contains an Azure policy designed to restrict available deployment types for Azure OpenAI, initially configured to limit the **Provisioned-Managed** type. The policy allows you to select and customize permitted deployment types based on your organization’s needs.

## Deployment Type Overview

Azure OpenAI offers three main deployment types, each optimized for different latency, throughput, and cost requirements:

- **Global Standard**: Configured for global routing, enabling real-time calls and high quotas, ideal for medium to high-volume use cases.
- **Standard**: Geared toward low to medium-volume workloads, with a pay-per-call model and flexibility for variable loads.
- **Provisioned Managed**: Allows specifying the required throughput for consistent, predictable workloads, with hourly billing and an option for monthly or yearly reservations.

## Purpose

With the growing adoption of AI, new deployment options emerge, not all of which are widely understood. This policy enhances governance by limiting deployment choices, helping to prevent unsuitable selections that may lead to unexpected costs or performance issues.

## How to Use

This policy is designed for easy integration and customization, allowing adjustments to permitted deployment types. The default configuration includes a list of allowed deployment types that can be edited to align with your organization’s guidelines.

## Policy Parameters

- **allowedSkus**: Defines the permitted deployment types (e.g., "Standard," "GlobalStandard").
- **effect**: Specifies the policy’s effect for unpermitted deployments (e.g., "AuditIfNotExists," "Deny").