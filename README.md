# terraform-aws-titan-hub ![Build Status][build.svg]

Terraform module implementing a Titan Hub for AWS.

A Titan Hub _is_ a [Titan Network][titan-network], intended to be used with one or more 
[Titan Environments][titan-environment] as the central hub in a hub-spoke architecture, with a single hub being the 
center of multiple environment networks. 

For example, a fairly typical setup would be:

 - `hub.mycompany.com`: the Titan Hub network
   - `dev.mycompany.com`: The Titan Environment for development resources.
   - `stg.mycompany.com`: The Titan Environment for staging resources.
   - `prod.mycompany.com`: The Titan Environment for production resources.

Typically, Titan Hubs serve as centralized resources available to all peered Titan Environments, so hosting an ELK stack
in the Titan Hub would be a good idea if it is desired that all environments send log traffic to one centralized ELK
cluster.

[Registry Link][registry]

## License

Licensed at your discretion under either:

 - [Apache Software License, Version 2.0](./LICENSE-APACHE)
 - [MIT License](./LICENSE-MIT)

 [build.svg]: https://github.com/naftulikay/terraform-aws-titan-hub/actions/workflows/ci.yml/badge.svg
 [titan-environment]: https://github.com/naftulikay/terraform-aws-titan-environment
 [titan-layer]: https://github.com/naftulikay/terraform-aws-titan-layer 
 [titan-hub]: https://github.com/naftulikay/terraform-aws-titan-hub
 [titan-network]: https://github.com/naftulikay/terraform-aws-titan-network
 [registry]: https://registry.terraform.io/modules/naftulikay/titan-hub/aws/latest