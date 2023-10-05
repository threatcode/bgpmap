# GoLang bindings for `bgp.he.net`

## Usage

```bash
go get github.com/ThreatCode/bgpmap
```

```golang
package main

import (
	"fmt"

	"github.com/ThreatCode/bgpmap"
)

func main() {
	// Search
	s := bgpmap.NewSearch("cloudflare")
	fmt.Println(s.ASNs)

	// Get IPv4 and IPv6 prefixes
	asn, err := bgpmap.NewASN(395747)
	if err != nil {
		fmt.Println(err)
		return
	}
	fmt.Println(asn.IPv4Networks)
	fmt.Println(asn.IPv6Networks)
}
```
