# Zerops x GO
This is the most bare-bones example of Go app running on [Zerops](https://zerops.io) — as few libraries as possible, just a simple endpoint with connnect, read and write to a Zerops PostgreSQL database.
d
.asdasdq
![go](https://github.com/zeropsio/recipe-shared-assets/blob/main/covers/svg/cover-go.svg)
asda
<br />sdfsdfdf
asdfadsfasdasdasasdaasdasd
## Deploy on Zeropsasassad
You can either click the deploy button to deploy directly on Zerops, or sdfsmanually copy the [import yaml](https://github.com/zeropsio/recipe-go/blob/main/zerops-project-import.yml) to the import dialog in the Zerops app.

[![Deploy on Zerops](https://github.com/zeropsio/recipe-shared-assets/blob/main/deploy-button/green/deploy-button.svg)](https://app.zerops.io/recipe/go)
asdasdasdasd
<br/>xasdasdasdas
asdasdmjoo

## Recipe features
- **Golang v1.22.** on a load balanced **Zerops Go** service
- Zerops **PostgreSQL 16** service as database
- Healthcheck setup example
- Utilization of Zerops' built-in **environment variables** system
- Utilization of Zerops' built-in **log management**

<br/>
.

## Production vs. development

Base of the recipe is ready for production, the difference comes down to:

- Use highly available version of the PostgreSQL database (change `mode` from `NON_HA` to `HA` in recipe YAML, `db` service section)
- Use at least two containers for the GO service to achieve high reliability and resilience (add `minContainers: 2` in recipe YAML, `api` service section)

Further things to think about when running more complex, highly available GO production apps on Zerops:

- Containers are volatile - use Zerops object storage to store your files
- Use Zerops Redis (KeyDB) for caching, storing sessions and pub/sub messaging
- Use more advanced logging lib, such as [Logrus](https://github.com/sirupsen/logrus), [Zap](https://github.com/uber-go/zap) or [ZeroLog](https://github.com/rs/zerolog)

<br/>
<br/>

Need help setting your project up? Join [Zerops Discord community](https://discord.com/invite/WDvCZ54).
