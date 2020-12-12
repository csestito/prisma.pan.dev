---
id: aws_rds
title: Amazon Relational Database Service
sidebar_label: RDS
description: Amazon Relational Database Service Queries
---

# Sample RQL Queries

:::note
The following guide will walk you through Amazon Relational Database Service RQL Query Examples
:::

## RDS Parameter group settings doesn't have the parameter: rds.force_ssl set

```bash
config where api.name = 'aws-rds-describe-db-parameter-groups' AND json.rule = ['parameters'].['rds.force_ssl'] does not exist
```

## RDS Aurora PostgreSQL is publicly accessible

```bash
config where api.name = 'aws-rds-db-cluster' AND json.rule = 'engine contains "aurora-postgresql" and publiclyAccessible is true'
```