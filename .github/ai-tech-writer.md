# ai-tech-writer — sf-template

- This repo is `nations-original/sf-template`, the official project template/skeleton for the Simple
  Framework (`composer create-project nations-original/sf-template`). Docs live in
  `nations-original/wiki` under `framework/`:
  - `framework/getting-started` — installation, `init.sh` / `install.sh`, constants, first page.
  - `framework/infrastructure` — docker-compose services, Redis/RabbitMQ, kernel config, template cache.
  - `framework/frontend` — webpack asset building.
  - `framework/dev` — Codeception suites, dev mode (`run.sh`).
- Source map: the `App/` skeleton (`Http/Controller`, `SymfonyControllers`, `Middleware`, `Entity`,
  `Repository`, `Enums`, `Kernel`), `config/` (`constants.php`, `packages/`, `routes.yaml`),
  `templates*/` (PHP class views, Twig, Blade), `init.sh` / `install.sh` / `run.sh`,
  `docker-compose.yml`, and the webpack config.
- Boundary: framework internals (routing, controllers, middleware, helpers, entities, validation) are
  documented from `nations-original/sf` (the package), not here — this repo documents the app skeleton
  and how it wires the framework. `framework/core/dual-kernel` is shared (app Symfony kernel here, SF
  kernel in sf).
- Template engines: three interchangeable view engines — PHP class views (`templates/`), Twig
  (`templates_twig/`), Blade (`templates_blade/`, via BladeOne). Keep the engine docs in sync with
  `App\Twig\PhpSfHelpersExtension`, the Blade CSRF/error wiring, and the example routes.
- Release semantics: composer package versioned by `vX.Y.Z` git tags, published to packagist as
  `nations-original/sf-template`; requires `nations-original/sf` (`^4.3`). Keep the README
  requirements/structure tables in sync with composer.json and `init.sh`.
