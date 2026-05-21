# Warn about partial matching
options(
  warnPartialMatchAttr = TRUE,
  warnPartialMatchDollar = TRUE,
  warnPartialMatchArgs = TRUE
)

# Load the usethis package if it's installed
if (interactive()) {
    require(usethis, quietly = TRUE)
}

if (interactive() && Sys.getenv("RSTUDIO") == "") {
  source(
    file.path(
      Sys.getenv(
        if (.Platform$OS.type == "windows")
          "USERPROFILE" else
            "HOME"
      ),
      ".vscode-R",
      "init.R"
    )
  )
}

if (interactive() && Sys.getenv("TERM_PROGRAM") == "vscode") {
  if ("httpgd" %in% .packages(all.available = TRUE)) {
    options(vsc.plot = FALSE)
    options(device = function(...) {
      httpgd::hgd(silent = TRUE)
      .vsc.browser(httpgd::hgd_url(history = FALSE), viewer = "Beside")
    })
  }
}

options(vsc.rstudioapi = TRUE)
