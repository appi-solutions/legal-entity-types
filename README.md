# Legal Entity Types

NPM package which lists legal entity types by country.

**Version**: `v1.0.0-alpha`

## Installation

NPM

```
npm install --save legal-entity-types
```

Yarn

```
yarn add legal-entity-types
```

## Usage

```javascript
const entities = require('legal-entity-types');
const country = 'FR'; // ISO 3166-1 alpha-2 code

console.log(entities[country].types);
/*
[{
  name: 'string',
  native: 'string',
  description: 'string'
}]
*/
```

## Contributing

See in [CONTRIBUTING.md](CONTRIBUTING.md).

## References

[[1] List of legal entity types by country](https://en.wikipedia.org/wiki/List_of_legal_entity_types_by_country)

## License

See in [LICENSE](LICENSE).
