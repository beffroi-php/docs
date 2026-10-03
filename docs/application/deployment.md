---
title: Deployment
status: draft
description: The image, FrankenPHP in worker mode, and the two planes.
---

# Deployment

The application runs on FrankenPHP in worker mode, with a process per plane when a deployment separates them,
PostgreSQL for the model and a broker for the asynchronous writes. TLS terminates in front of it, and the
listener that asks for a client certificate is a host of its own.

This page will describe the image, the processes, the health checks, and the reverse proxy.
