// === README.md ===
// Material Conversion Worker for Respina Smart Services Inc.
// Rust 2021 | glTF RS | tokio | ktx2 | image | anyhow | clap
//
// This command‑line tool reads a glTF file, converts all referenced textures to KTX2,
// and generates simple grayscale lightmaps of configurable size.
//
// Prerequisites:
//   • Rust 1.66 or later
//   • Cargo
//
// Build:
//   cargo build --release
//
// Usage:
//   ./target/release/material_converter \
//       --input model.gltf \
//       --output-dir out_textures \
//       --lightmap-size 512
//
// Arguments:
//   --input         Path to .gltf or .glb model
//   --output-dir    Directory to emit .ktx2 and lightmap.png files
//   --lightmap-size Width/height in pixels for generated lightmaps
//
// All output files are named:
//   texture_{index}.ktx2
//   lightmap_{index}.png

// === Cargo.toml ===
// [package]
// name = "material_converter"
// version = "0.1.0"
// edition = "2021"
//
// [dependencies]
// tokio = { version = "1", features = ["full"] }
// gltf = "0.15"
// image = "0.24"
// ktx2 = "0.5"
// anyhow = "1.0"
// clap = { version = "4.2", features = ["derive"] }
