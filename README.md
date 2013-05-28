## hdf2json

Simple Python tool that we wrote to help with the transition of Clearsilver's HDF dataset to the more popular JSON format

[Read the blog post](http://www.discogs.com/blog/transitioning-from-hdf-to-json)

### Usage

HDF data to JSON:

```bash
>>> from hdf2json import hdf2json
>>> hdf2json(release_hdf_data)
'{"labels": [{"catno": "SK032", "name": "Svek"}], "title": "Stockholm"}'
```

HDF data to a native Python dictionary:

```bash
>>> from hdf2json import hdf2dict
>>> release = hdf2dict(release_hdf_data)
>>> release['title']
Stockholm
```

And then back to JSON:

```bash
>>> json.dumps(release)
'{"labels": [{"catno": "SK032", "name": "Svek"}], "title": "Stockholm"}'
```
