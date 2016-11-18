# NPOKit Extra Resources

This repository contains a curated list of additional resources for programs broadcasted by the Dutch Public Broadcaster (NPO).

## Contributing

In order to contribute new resources, [fork](https://github.com/4np/NPOKitResources#fork-destination-box) this repository and add the addition resource(s) to the [JSON document](https://github.com/4np/NPOKitResources/blob/master/ProgramResources.json). When done, make sure to [validate](http://jsonlint.com) the updated JSON document before submitting a pull request.

## Format

A recource consist of a program `mid` (which you can lookup [here](http://apps-api.uitzendinggemist.nl/series.json)), its name and a description of that resource. Currently only youtube channels are users are supported.

### An example of a YouTube _channel_ resource

```
{
	"mid": "VPWON_1250334",
	"name": "Zondag met Lubach",
	"youtube": {
		"channel": "UCdH_8mNJ9vzpHwMNwlz88Zw"
	}
}
```

### An example of a YouTube _user_ resource

```
{
	"mid": "VPWON_1250305",
	"name": "VPRO Tegenlicht",
	"youtube": {
		"user": "VPROTegenlicht"
	}
}
```