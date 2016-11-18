# NPOKit Extra Resources

This repository contains a curated list of additional resources for programs broadcasted by the Dutch Public Broadcaster (NPO).

## Contributing

In order to contribute new resources, [fork](https://github.com/4np/NPOKitResources#fork-destination-box) this repository and add the addition resource(s) to the [JSON document](https://github.com/4np/NPOKitResources/blob/master/ProgramResources.json). When done, make sure to [validate](http://jsonlint.com) the updated JSON document before submitting a pull request.

## Format

A recource consist of a program `mid` (which you can lookup [here](http://apps-api.uitzendinggemist.nl/series.json)), its name and a description of that resource. Currently only youtube channels are users are supported.

### An example of a YouTube channel resource

[Zondag met Lubach](https://www.youtube.com/channel/UCdH_8mNJ9vzpHwMNwlz88Zw) has a URL in the following format:

```
https://www.youtube.com/channel/UCdH_8mNJ9vzpHwMNwlz88Zw
```

The Channel Identifier for this YouTube channel is `UCdH_8mNJ9vzpHwMNwlz88Zw`, which you can use to add a new element to the JSON file:


```
{
	 "mid": "VPWON_1250334",
     "name": "Zondag met Lubach",
     "youtube_channel": "UCdH_8mNJ9vzpHwMNwlz88Zw"
}
```

### Finding the right channel identifier

The channel identifier looks like a random string. Whenever you see something readable it generally is *_not_* the channel identifier.

Sometimes the channel identifier is conveniently in the URL, but more often it is not. Sometimes you will see it when you subscribe to a channel, but the best way is to view the source of the channel page and search for an entry like this:

```
<link rel="alternate" type="application/rss+xml" title="RSS" href="https://www.youtube.com/feeds/videos.xml?channel_id=UC6gpEAIMMzVQZU4G86G7wVQ">
```

In this case the channel identifier is `UC6gpEAIMMzVQZU4G86G7wVQ` (De Wereld Draait Door).

### Testing the channel identifier

When you have found the channel identifier, test if it works by opening the following url and replacing `channel_identifier` with the found identifier:

```
https://www.youtube.com/channel/channel_identifier
```