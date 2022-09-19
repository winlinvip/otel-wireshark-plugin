# otel-wireshark-plugin

Wireshark plugin for OpenTelemetry(otel).

## Usage

Setup wireshark plugin:

```bash
cd ~/git
git clone https://github.com/winlinvip/otel-wireshark-plugin.git
cd ~/git/otel-wireshark-plugin

mkdir -p ~/.local/lib/wireshark/plugins
ln -sf $(pwd)/otel.lua ~/.local/lib/wireshark/plugins/otel.lua
```

Setup protobuf for otel APM:

```bash
cd ~/git
git clone https://github.com/open-telemetry/opentelemetry-proto.git

cd ~/git
git clone https://github.com/ossrs/srs.git
```

Setup Wireshark `Protobuf search paths` to load the proto files at `Preferences > Protocols > Protobuf`:
* `/Users/winlin/git/opentelemetry-proto`
* `/Users/winlin/git/srs/trunk/research/proto`

> Note: Please use absolute path, never use `~` or `$HOME`.

Start capture or parsing file.
