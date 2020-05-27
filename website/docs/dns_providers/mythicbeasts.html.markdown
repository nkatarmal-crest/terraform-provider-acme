---
layout: "acme"
page_title: "ACME: MythicBeasts DNS Challenge Provider"
sidebar_current: "docs-acme-dns-providers-mythicbeasts"
description: |-
  Provides a resource to manage certificates on an ACME CA.
---
<br>

-> **NOTE:** The following documentation is auto-generated from the
ACME provider's API library [lego](https://go-acme.github.io/lego/).
Some sections may refer to lego directly - in most cases, these
sections apply to the Terraform provider as well.

# MythicBeasts DNS Challenge Provider

The `mythicbeasts` DNS challenge provider can be used to perform DNS challenges for
the [`acme_certificate`][resource-acme-certificate] resource with
[MythicBeasts](https://www.mythic-beasts.com/).

[resource-acme-certificate]: /docs/providers/acme/r/certificate.html

For complete information on how to use this provider with the `acme_certifiate`
resource, see [here][resource-acme-certificate-dns-challenges].

[resource-acme-certificate-dns-challenges]: /docs/providers/acme/r/certificate.html#using-dns-challenges

## Example

```hcl
resource "acme_certificate" "certificate" {
  ...

  dns_challenge {
    provider = "mythicbeasts"
  }
}
```
## Argument Reference

The following arguments can be either passed as environment variables, or
directly through the `config` block in the
[`dns_challenge`][resource-acme-certificate-dns-challenge-arg] argument in the
[`acme_certificate`][resource-acme-certificate] resource. For more details, see
[here][resource-acme-certificate-dns-challenges].

[resource-acme-certificate-dns-challenge-arg]: /docs/providers/acme/r/certificate.html#dns_challenge

In addition, arguments can also be stored in a local file, with the path
supplied by supplying the argument with the `_FILE` suffix. See
[here][acme-certificate-file-arg-example] for more information.

[acme-certificate-file-arg-example]: /docs/providers/acme/r/certificate.html#using-variable-files-for-provider-arguments

* `MYTHICBEASTS_PASSWORD` - Paswword.
* `MYTHICBEASTS_USERNAME` - User name.

* `MYTHICBEASTS_API_ENDPOINT` - The endpoint for the API (must implement v2).
* `MYTHICBEASTS_HTTP_TIMEOUT` - API request timeout.
* `MYTHICBEASTS_POLLING_INTERVAL` - Time between DNS propagation check.
* `MYTHICBEASTS_PROPAGATION_TIMEOUT` - Maximum waiting time for DNS propagation.
* `MYTHICBEASTS_TTL` - The TTL of the TXT record used for the DNS challenge.
* `MYTHICBEASYS_AUTH_API_ENDPOINT` - The endpoint for Mythic Beasts' Authentication.

If you are using specific API keys, then the username is the API ID for your API key, and the password is the API secret.

Your API key name is not needed to operate lego.

