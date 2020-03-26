# Ukpik API documentation

The API documentation is based on [OpenAPI 3.0.0](https://swagger.io/).

The API server: [https://vision.ukpik.ai/v1](https://vision.ukpik.ai/v1)
The API documentation website [https://docs.ukpik.ai](https://docs.ukpik.ai)

## Work with API

To work with API you need `API_KEY`. Please contact us contact@jalgos.com to have access.

The classification uses `analyse id` parameter that should be a unique number for each request. You can use a continuously growing counter.

## Use scripts

Classification API is asynchronous. The general flow is to send video to classification and receive the result by calling `/result` endpoint or using webhook

Clone repository

```bash
git clone git@github.com:jalgos/ukpik-api-docs.git
cd ukpik-api-docs
```

Add `API_KEY` to environment variables

```bash
export API_KEY="YOUR API KEY"
```

### Post video

Usage

```bash
bin/post-video $endpoint $analyse_id $video_path $metadata_path
```

Example

```bash
bin/post-video https://vision.ukpik.ai/v1 1254448 bin/video.mov bin/metadata.json
```

### Get results

Usage

```bash
bin/post-labels $server $analyse_id $labels_path
```

Example

```bash
bin/post-labels https://vision.ukpik.ai/v1 1254448 bin/labels.json
```
