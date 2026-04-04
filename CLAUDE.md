# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio and blog site hosted at https://andrewsimone.com via GitHub Pages. Static site — no build step, no package manager, no dependencies to install.

## Deployment

Push to `main` and GitHub Pages deploys automatically. No CI/CD pipeline.

## Architecture

- `index.html` — Homepage/portfolio. Self-contained: all CSS is embedded in a `<style>` block, no external stylesheet, no JavaScript.
- `resume.html` — Resume page. Same self-contained design pattern as `index.html`. Has `noindex, nofollow` robots meta.
- `the-myth-of-sisyphus.html`, `the-retro-console.html` — Blog posts.
- `dnd/` — D&D campaign site based on the "Alpha" theme from HTML5 UP. Uses jQuery + skel.js for responsive layout. Contains HTML comment placeholders (e.g. `<!-- CAMPAIGN_TITLE -->`) for campaign-specific content.
- `dnd-archive/waterdeep/` — Archived prior campaign.
- `CNAME` — Maps GitHub Pages to `andrewsimone.com`.

## Design Conventions

The main pages (`index.html`, `resume.html`) share a consistent visual style:
- Google Fonts: Work Sans
- CSS `clamp()` for fluid typography and spacing
- CSS Grid and Flexbox for layout
- All styles embedded directly in `<style>` tags — no separate stylesheet

The `dnd/` section uses a different pattern: external CSS files in `dnd/css/` with responsive breakpoint variants (`style-wide.css`, `style-normal.css`, `style-narrow.css`, `style-mobile.css`).
