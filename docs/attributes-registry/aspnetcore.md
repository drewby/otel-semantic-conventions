<!--- Hugo front matter used to generate the website version of this page:
--->

<!-- NOTE: THIS FILE IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/attribute_namespace.md.j2 -->

# Aspnetcore

## ASP.NET Core Attributes

ASP.NET Core attributes

| Attribute                                 | Type    | Description                                                                                                                                                                       | Examples                       | Stability                                                  |
| ----------------------------------------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ | ---------------------------------------------------------- |
| `aspnetcore.diagnostics.exception.result` | string  | ASP.NET Core exception middleware handling result                                                                                                                                 | `handled`; `unhandled`         | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `aspnetcore.diagnostics.handler.type`     | string  | Full type name of the [`IExceptionHandler`](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.diagnostics.iexceptionhandler) implementation that handled the exception. | `Contoso.MyHandler`            | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `aspnetcore.rate_limiting.policy`         | string  | Rate limiting policy name.                                                                                                                                                        | `fixed`; `sliding`; `token`    | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `aspnetcore.rate_limiting.result`         | string  | Rate-limiting result, shows whether the lease was acquired or contains a rejection reason                                                                                         | `acquired`; `request_canceled` | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `aspnetcore.request.is_unhandled`         | boolean | Flag indicating if request was handled by the application pipeline.                                                                                                               | `true`                         | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `aspnetcore.routing.is_fallback`          | boolean | A value that indicates whether the matched route is a fallback route.                                                                                                             | `true`                         | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `aspnetcore.routing.match_status`         | string  | Match result - success or failure                                                                                                                                                 | `success`; `failure`           | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |

`aspnetcore.diagnostics.exception.result` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value       | Description                                                      | Stability                                                  |
| ----------- | ---------------------------------------------------------------- | ---------------------------------------------------------- |
| `aborted`   | Exception handling didn't run because the request was aborted.   | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `handled`   | Exception was handled by the exception handling middleware.      | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `skipped`   | Exception handling was skipped because the response had started. | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `unhandled` | Exception was not handled by the exception handling middleware.  | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |

`aspnetcore.rate_limiting.result` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value              | Description                                        | Stability                                                  |
| ------------------ | -------------------------------------------------- | ---------------------------------------------------------- |
| `acquired`         | Lease was acquired                                 | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `endpoint_limiter` | Lease request was rejected by the endpoint limiter | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `global_limiter`   | Lease request was rejected by the global limiter   | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `request_canceled` | Lease request was canceled                         | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |

`aspnetcore.routing.match_status` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value     | Description     | Stability                                                  |
| --------- | --------------- | ---------------------------------------------------------- |
| `failure` | Match failed    | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
| `success` | Match succeeded | ![Stable](https://img.shields.io/badge/-stable-lightgreen) |
