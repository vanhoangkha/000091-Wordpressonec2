# Deploy WordPress to an Amazon EC2 instance using CodeDeploy

> Hosting WordPress on Amazon EC2.

A hands-on workshop from the [AWS First Cloud Journey](https://github.com/vanhoangkha/aws-first-cloud-journey) series, available in English and Vietnamese.

**Read the workshop online:** https://vanhoangkha.github.io/000091-Wordpressonec2/

## Overview

In this workshop, you deploy WordPress, an open source blogging engine and content management system based on PHP and MySQL, to a single Amazon EC2 running Amazon Linux or Red Hat Enterprise Linux (RHEL).

AWS CodeDeploy is a fully managed deployment service that automates software deployment across compute services like Amazon EC2, AWS Fargate, AWS Lambda, and your on-premises servers. AWS CodeDeploy makes it easier to quickly release new features, avoid downtime during application deployment, and make it simpler to update your application. You can use AWS CodeDeploy to automate software deployments and eliminate the need for error-prone manual tasks. The service scales to fit your deployment needs.

## Workshop contents

1. Introduction
2. Preparation
   - Create access key
   - Create instance profile
   - Create service role
3. Launch an EC2 instance
4. Installing CodeDeploy Agent
5. Create S3 bucket
6. Create deployment group
7. Deploy the WordPress App
8. Clean up resources

## Prerequisites

- An AWS account with permissions to create the resources used in the labs
- Basic familiarity with the AWS Management Console
- [Hugo](https://gohugo.io/installation/) (extended edition) if you want to run the site locally

## Run locally

```bash
git clone --recurse-submodules https://github.com/vanhoangkha/000091-Wordpressonec2.git
cd 000091-Wordpressonec2
hugo server
```

Then open http://localhost:1313 in your browser.

## Repository structure

| Path | Purpose |
| --- | --- |
| `content/` | Workshop pages (`*.md` English, `*.vi.md` Vietnamese) |
| `static/` | Images and other static assets |
| `layouts/` | Hugo layout overrides |
| `themes/` | Hugo theme |
| `config.toml` | Site configuration |

## Cost and cleanup

The labs create AWS resources that may incur charges. Complete the **Clean up** chapter when you finish to remove them.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

To report a security issue, see [SECURITY.md](SECURITY.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
