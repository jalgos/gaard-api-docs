# Gaard API documentation

The API documentation is based on [OpenAPI 3.0.0](https://swagger.io/).

- API server: [https://vision.gaard.ai/v1](https://vision.gaard.ai/v1)
- API documentation website [https://docs.gaard.ai](https://docs.gaard.ai)

## Work with API

To work with API you need `API_KEY`. Please contact us contact@jalgos.com to have access.

The classification uses `analyse_id` parameter that should be a unique number for each request. You can use a continuously growing counter.

## Use scripts

Classification API is asynchronous. The general flow is to send video to classification and receive the result by calling `/result` endpoint or using webhook

Clone repository

```bash
git clone git@github.com:jalgos/gaard-api-docs.git
cd gaard-api-docs
```

Add `API_KEY` to environment variables

```bash
export API_KEY="YOUR API KEY"
```

### Post video

Usage

```bash
bin/post-video [video_path] [analyse_id] [metadata_path]
```

Examples

```bash
bin/post-video
bin/post-video bin/video.mov
bin/post-video bin/video.mov 1254448
bin/post-video bin/video.mov 1254448 bin/metadata.json
```

### Get results

Usage

```bash
bin/get-result analyse_id
```

Example

```bash
bin/get-result 1254448
```

### Get original video

Usage

```bash
bin/get-original-video filename
```

Example

```bash
bin/get-original-video video.mov
```

### Get Highlighted video

Usage

```bash
bin/get-highlighted-video filename
```

Example

```bash
bin/get-highlighted-video video.mov
```

## Licenses

An example `bin/video.mov` is a part of [The VIRAT Video Dataset](https://viratdata.org/)
