---
# try also 'default' to start simple
theme: default
presenter: true
title: 'Cloud Computing | Compute and Storage'
titleTemplate: '%s - CPIT-490'
# apply any windi css classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: | 
    Cloud Computing | Compute and Storage
# page transition
transition: slide-left
# use UnoCSS
css: unocss
# Make content selectable/copyable
selectable: true
favicon: '/images/favicon.ico'
# Make slides downloadable as PDF
download: true
exportFilename: cloud-computing-slides
export:
  format: pdf
  timeout: 30000
  dark: false
  withClicks: false
  withToc: false
# enable slide recording and drawing
record: build
drawings:
  enabled: true
  persist: false
  presenterOnly: false
  syncAll: true

# open graph
seoMeta:
  # By default, Slidev will use ./og-image.png if it exists,
  # or generate one from the first slide if not found.
  ogImage: auto
  # ogImage: https://cover.sli.dev
---

# System Administration

### CPIT-490/632: Cloud Computing Architecture


<div class="absolute left-30px bottom-30px">
Fall 2025 &copy; Khalid Alharbi, Ph.D.
</div>

---
src: ./pages/imported-slides.md
---