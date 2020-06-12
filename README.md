# Simple S3 client

Simple client for personal projects.

Usage:

```
$s3 = new \Umonkey\S3([
    'bucket' => 'foobar',
    'bucket_region' => 'ru-central1',
    'acl' => 'public-read',
    'access_key' => null,
    'secret_key' => null,
    'endpoint' => 'storage.yandexcloud.net',
]);

list($status, $output, $url) = $s3->putObject('videos/example.mp4', __DIR__ . '/video.mp4', [
    'content-type' => 'video/mpeg4',
]);

if ($status === 200) {
    var_dump($url);
}
```
