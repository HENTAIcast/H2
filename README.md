# b/
serde = { version = "1.0.134", features = ["derive"] }
serde_json = "1.0.78"
tempfile = "3.3.0"
term_size = "0.3.2"
terminal_size = "0.3"
textwrap = "0.16"
tokio = { version = "1.14", features = ["fs", "macros", "process", "rt-multi-thread"] }
toml = "0.8"
  20 changes: 12 additions & 8 deletions20  
src/output.rs
Original file line number	Diff line number	Diff line change
@@ -3,6 +3,7 @@ use std::io::{stdout, Write};

use bodhi::{Comment, Update};
use chrono::{DateTime, Duration, Utc};
use terminal_size::{terminal_size, Width};

use crate::parse::parse_nvr;

