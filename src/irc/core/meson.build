# this file is part of irssi

libirc_core_a = static_library('irc_core',
  files(
    'bans.c',
    'channel-events.c',
    'channel-rejoin.c',
    'channels-query.c',
    'ctcp.c',
    'irc-cap.c',
    'irc-channels-setup.c',
    'irc-channels.c',
    'irc-chatnets.c',
    'irc-commands.c',
    'irc-core.c',
    'irc-expandos.c',
    'irc-masks.c',
    'irc-nicklist.c',
    'irc-queries.c',
    'irc-servers-reconnect.c',
    'irc-servers-setup.c',
    'irc-servers.c',
    'irc-session.c',
    'irc.c',
    'lag.c',
    'massjoin.c',
    'mode-lists.c',
    'modes.c',
    'netsplit.c',
    'sasl.c',
    'servers-idle.c',
    'servers-redirect.c',
  ),
  include_directories : rootinc,
  implicit_include_directories : false,
  c_args : [
    def_moduledir,
    def_sysconfdir,
  ],
  dependencies : dep)
libirc_core_sm = shared_module('irc_core',
  install : true,
  install_dir : moduledir,
  link_whole : libirc_core_a)

dl_cross_irc_core = []
if need_dl_cross_link
  dl_cross_irc_core += libirc_core_sm
endif

install_headers(
  files(
    'bans.h',
    'channel-events.h',
    'channel-rejoin.h',
    'ctcp.h',
    'irc-cap.h',
    'irc-channels.h',
    'irc-chatnets.h',
    'irc-commands.h',
    'irc-masks.h',
    'irc-nicklist.h',
    'irc-queries.h',
    'irc-servers-setup.h',
    'irc-servers.h',
    'irc.h',
    'mode-lists.h',
    'modes.h',
    'module.h',
    'netsplit.h',
    'sasl.h',
    'servers-idle.h',
    'servers-redirect.h',
  ),
  subdir : incdir / 'src' / 'irc' / 'core')
