# terraform-crds-manager

## 1.0.0

- Replace `gavinbunney/kubectl` with `alekc/terraform-provider-kubectl`; this will cause resources to be recreated (and thus the major version bump), but you can avoid that importing them in the new provider following [the linked guide][0];
- Require Terraform 0.13 or newer;

[0]: https://github.com/alekc/terraform-provider-kubectl?tab=readme-ov-file#changing-providers-for-existing-resources

## 0.3.0

With this release, a new variable is available:
- `apply_only`: if true, no CRD will be ever deleted by the module. Default to `false`;

Updating the module doesn't change the current behavior.

## 0.2.0

Thanks to @joelsdc for their first contribution!

With this release, two new variables are available:
— `force_new`: Forces delete & create of resources if the `yaml_body` changes;
— `force_conflicts`: Allows using `force_conflicts`;

Both of them are optional, and default to false, so updating the module doesn't change the behavior.