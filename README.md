# Spring Boot File Upload & Download API

## 1. Description
This is the description of the file upload API:
- End point URI: /uploadFile
- HTTP method: POST
- Request body has a parameter named “file” along with multipart file data.
- Response status:
  + BAD_REQUEST if the request doesn’t contain multipart file data
  + METHOD_NOT_ALLOWED if the request method is not POST
  + INTERNAL_SERVER_ERROR if any IO error occurs on the server
  + OK if upload successful, with the following JSON:

```json
{
    "fileName": "ed414a169f02ba144b8112c47a4c3774c94ad52cv2_hq.jpg",
    "downloadUri": "/downloadFile/DDKYoXmD",
    "size": 11767
}
```

Note that the alphanumeric string at the end of the downloadUri field is the file code which is used in file download API.
And below is description of the file download API:
- End point URI: /downloadFile/{fileCode}
- HTTP method: GET
- Response status:
  + NOT_FOUND if no file found for the given file code
  + METHOD_NOT_ALLOWED if the request method is not POST
  + INTERNAL_SERVER_ERROR if any IO error occurs on the server
  + OK if a file found and the response contains file data


## 2. Install
```sh
git clone https://github.com/EfrainGaray/springboot-fileupload-main.git
```
Download dependency and play :love_you_gesture:

## License

MIT

