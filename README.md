## Beat Output Pulsar

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdouglarek%2Fbeat-pulsar-output.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdouglarek%2Fbeat-pulsar-output?ref=badge_shield)

This project is cloned from [streamnative/pulsar-beat-output](https://github.com/streamnative/pulsar-beat-output), and separated into independent outputs to facilitate joint compilation with the mainline beat; the license inherits from the original repository.

### How to use

For example, let's consider filebeat (tested in the latest 7.x branch):

```diff
--- filebeat/main.go	2023-03-14 13:30:19.614554664 +0800
+++ main.go	2023-03-14 13:29:45.404568706 +0800
@@ -20,6 +20,7 @@
 import (
 	"os"
 
+	_ "github.com/douglarek/beat-pulsar-output/pulsar"
 	"github.com/elastic/beats/v7/filebeat/cmd"
 	inputs "github.com/elastic/beats/v7/filebeat/input/default-inputs"
 )
 ```

## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdouglarek%2Fbeat-pulsar-output.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdouglarek%2Fbeat-pulsar-output?ref=badge_large)
