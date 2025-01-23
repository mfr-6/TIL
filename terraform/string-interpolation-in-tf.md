### String Interpolation in Terraform
---

To put a variable inside the string using string interpolation, you need to reference it using 
`${ ... }` syntax:

```HCL
"Hello, ${var.name}"
```
