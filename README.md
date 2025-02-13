# Statuspage Exporter
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fsergeyshevch%2Fstatuspage-exporter.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fsergeyshevch%2Fstatuspage-exporter?ref=badge_shield)


Statuspage exporter exports metrics from given statuspages as prometheus metrics.

## Supported statuspage engines:
- Statuspage.io (Widely used statuspage engine. For example by [GitHub](https://www.githubstatus.com)). You can check that statuspage is supported by this engine by checking that it has a [/api/v2/components.json](https://www.githubstatus.com/api/v2/components.json) endpoint.

## Some popular statuspages:
- [GitHub](https://www.githubstatus.com)
- [Atlassian (Jira/Confluence/etc)](https://status.atlassian.com/)

## Metrics Example
```
# HELP service_status Status of a service component, values 0 (operational) to 4 (major_outage)
# TYPE service_status gauge
service_status{component="API Requests",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Actions",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Codespaces",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Copilot",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Git Operations",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Issues",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Packages",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Pages",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Pull Requests",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Visit www.githubstatus.com for more information",service="GitHub",status_page_url="https://status.github.com"} 1
service_status{component="Webhooks",service="GitHub",status_page_url="https://status.github.com"} 1
# HELP statuspage_exporter_build_info A metric with a constant '1' value labeled by version, revision, branch, and goversion from which statuspage_exporter was built.
# TYPE statuspage_exporter_build_info gauge
statuspage_exporter_build_info{branch="",goversion="go1.19.2",revision="",version=""} 1
```





## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fsergeyshevch%2Fstatuspage-exporter.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fsergeyshevch%2Fstatuspage-exporter?ref=badge_large)