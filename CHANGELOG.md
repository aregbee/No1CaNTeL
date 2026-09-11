# Kodi VPN Manager Changelog

## 0.1.1~beta17 - 2026-09-10

### Added
- Automatic VPN watchdog for protected router/local VPN recovery.
- Lightweight router exit-IP monitoring.
- Physical-WAN recovery probing to distinguish detector failure from upstream failure.
- Backoff/recovery handling for temporary WAN and DNS outages.
- Protected router-to-local OpenVPN fallback.
- Automatic local OpenVPN-to-router VPN recovery.
- Exact preflighted OpenVPN endpoint pinning.
- Runtime target handoff for managed OpenVPN.
- Profile Manager three-column layout and protected profile activation workflow.

### Changed
- Replaced frequent full selector polling with lightweight Kodi-service monitoring.
- Local OpenVPN fallback now uses the same exact preflighted endpoint for the launcher and kill switch.
- Improved router/local handoff transaction and verification logic.
- Improved profile preflight and rollback behavior.
- Old vpn-selector systemd timer remains disabled.

### Fixed
- Prevented repeated full selector runs during temporary WAN/DNS outages.
- Fixed missing backend time/socket dependencies encountered during transaction testing.
- Improved fail-closed handling when physical Internet is unavailable.
- Improved deterministic rollback to the previous protected VPN path.
- Improved DNS-lock and kill-switch coordination during local fallback.

### Verified
- Real router VPN -> local OpenVPN automatic failover.
- Real local OpenVPN -> verified router VPN automatic failback.
- Fail-closed behavior during physical upstream outage.
- Pinned OpenVPN endpoint, kill switch, DNS lock, routing, and tun0 state.
- Profile switching and router-managed fallback selection.

## 0.1.1~beta16

- Previous published beta.
- Repository packaging and distribution baseline used for beta17 development.
