# s3buddy

Screenshot and file sharing scripts for S3 and MATE

## Included Scripts

* `selectionupload` - screenshot a selection, upload it to S3 and copy the destination URL to the clipboard.
* `screenupload` - screenshot the whole screen, upload it to S3 and copy the destination URL to the clipboard. Will wait 1 second before taking a screenshot.
* `quickupload` - upload a file to S3 and copy the destination URL to the clipboard. Requires a file to be given, e.g. `quickupload image.png`.

## Usage

All scripts require MATE (for `mate-screenshot`), a mechanism to send notifications (for `notify-send`) and a configured instance of the [AWS CLI tools version 2](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

### Variables

All scripts share the same variables included in the header that need to be configured before use.

|Variable|Description|Example|
|-|-|-|
|`S3BUCKET`|S3 bucket to upload files to.|`example-bucket`|
|`S3PATH`|Path in the S3 bucket to upload files to, for root use `/`.|`/uploads/`|
|`S3ARGS`|Any optional arguments for the AWS CLI.|`--profile uploads`|
|`URL`|Destination URL that mirrors your bucket, e.g. the static URL for your bucket in properties.|`https://example-bucket.s3.amazonaws.com`|

### Installation

Once the variables have been configured you can copy the scripts anywhere in your path (e.g. `/usr/local/bin`) to run them from your terminal.

On MATE you can also add a "Custom Application Launcher" to your top panel which can run each script. If you're using Numix (the default on Ubuntu MATE), I have found `/usr/share/icons/Numix-Light/24/status/simplescreenrecorder-idle.svg` to be a great screenshot icon. I have also tried running the scripts as MATE keyboard shortcuts but have ran into issues, your mileage may vary.

