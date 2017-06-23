# Conky sample configuration
# Made by Santu Haldar.
# Change your network device accroding to your ifconfig on ln no 164,165,166

# set to yes if you want Conky to be forked in the background
#background yes

# X font when Xft is disabled, you can pick one with program xfontsel
#font 5x7
#font 6x10
#font 7x13
#font 8x13
#font 9x15
#font *mintsmild.se*
#font -*-*-*-*-*-*-34-*-*-*-*-*-*-*

# Use Xft?
use_xft yes

# Xft font when Xft is enabled
xftfont Bitstream Vera Sans Mono:size=8

# Text alpha when using Xft
xftalpha 0.8

# Print everything to stdout?
# out_to_console no

# MPD host/port
# mpd_host localhost
# mpd_port 6600
# mpd_password tinker_bell

# Print everything to console?
# out_to_console no

# mail spool
mail_spool $MAIL

# Update interval in seconds
update_interval 1.0

# This is the number of times Conky will update before quitting.
# Set to zero to run forever.
total_run_times 0

# Create own window instead of using desktop (required in nautilus)
own_window yes
#own_window no

# If own_window is yes, you may use type normal, desktop or override
#own_window_type desktop
own_window_type normal

# Use pseudo transparency with own_window?
#own_window_transparent yes
own_window_transparent no

# If own_window_transparent is set to no, you can set the background colour here
# own_window_colour hotpink

# If own_window is yes, these window manager hints may be used
#own_window_hints undecorated,below,sticky,skip_taskbar,skip_pager

# Use double buffering (reduces flicker, may not work for everyone)
double_buffer yes

# Minimum size of text area
minimum_size 280 5

# Draw shades?
draw_shades yes

# Draw outlines?
draw_outline no

# Draw borders around text
draw_borders no

# Draw borders around graphs
draw_graph_borders yes

# Stippled borders?
stippled_borders 8

# border margins
border_margin 4

# border width
border_width 0

# Default colors and also border colors
default_color white
default_shade_color black
default_outline_color black

# Text alignment, other possible values are commented
#alignment top_left
alignment top_right
#alignment bottom_left
#alignment bottom_right
#alignment none

# Gap between borders of screen and text
# same thing as passing -x at command line
gap_x 12
gap_y 12

# Subtract file system buffers from used memory?
no_buffers yes

# set to yes if you want all text to be in uppercase
uppercase no

# number of cpu samples to average
# set to 1 to disable averaging
cpu_avg_samples 2

# number of net samples to average
# set to 1 to disable averaging
net_avg_samples 2

# Force UTF8? note that UTF8 support required XFT
override_utf8_locale no

# Add spaces to keep things from moving about?  This only affects certain objects.
use_spacer none

# Allow each port monitor to track at most this many connections (if 0 or not set, default is 256)
#max_port_monitor_connections 256

# Maximum number of special things, e.g. fonts, offsets, aligns, etc.
#max_specials 512

# Maximum size of buffer for user text, i.e. below TEXT line.
#max_user_text 16384

# Timing interval for music player thread, e.g. mpd, audacious
#music_player_interval (update_interval is default)

# variable is given either in format $variable or in ${variable}. Latter
# allows characters right after the variable and must be used in network
# stuff because of an argument

# stuff after 'TEXT' will be formatted on screen

TEXT
$nodename - $sysname $kernel on $machine
Time: ${alignr} ${color 00ff00} $time
$stippled_hr
${color lightgrey}Uptime:${color #00ff00} $uptime ${color lightgrey} ${alignr} Load:${color 00ff00} ${freq 1}MHz ${color 00ff00} ${freq 2}MHz
${color lightgrey}CPU Usage:${color #00ff00} $cpu% ${color lightgrey}${cpubar}
${color black}${cpugraph 0000ff 00ff00}
${color black}${loadgraph 0000ff 00ff00}
${color lightgrey}RAM Usage:$color $mem/$memmax - $memperc% ${membar}
${color lightgrey}Swap Usage:$color $swap/$swapmax - $swapperc% ${swapbar}
${color lightgrey}Processes:$color $processes  ${color grey}Running:$color $running_processes
$color$stippled_hr
${color lightgrey}Networking:
# Up:${color #8844ee} ${upspeed enp2s0} k/s ${offset 80}${color lightgrey}
 Down:${color 00ff00} ${alignr} ${downspeed enp2s0} ${color lightgrey}k/s${color lightgrey}
${color #0000ff}${upspeedgraph enp2s0 32,150 ff0000 lightgrey} ${color #22ccff}${downspeedgraph enp2s0 32,150 0000ff 00ff00}
${color lightgrey}File systems:
 / $color${fs_used /}/${fs_size /} ${fs_bar /}
${color}Name ${alignr} PID   CPU%   MEM%
${color #00ff00} ${top name 1} ${alignr} ${top pid 1} ${top cpu 1} ${top mem 1}
${color lightgrey} ${top name 2} ${alignr} ${top pid 2} ${top cpu 2} ${top mem 2}
${color lightgrey} ${top name 3} ${alignr} ${top pid 3} ${top cpu 3} ${top mem 3}
${color lightgrey} ${top name 4} ${alignr} ${top pid 4} ${top cpu 4} ${top mem 4}
${color lightgrey} ${top name 5} ${alignr} ${top pid 5} ${top cpu 5} ${top mem 5}
${color lightgrey} ${top name 6} ${alignr} ${top pid 6} ${top cpu 6} ${top mem 6}
${color lightgrey} ${top name 7} ${alignr} ${top pid 7} ${top cpu 7} ${top mem 7}
${color}Mem usage
${color #ddaa00} ${top_mem name 1} ${alignr} ${top_mem pid 1} ${top_mem cpu 1} ${top_mem mem 1}
${color lightgrey} ${top_mem name 2} ${alignr} ${top_mem pid 2} ${top_mem cpu 2} ${top_mem mem 2}
${color lightgrey} ${top_mem name 3} ${alignr} ${top_mem pid 3} ${top_mem cpu 3} ${top_mem mem 3}
#$stippled_hr
#${color #ddaa00}Outbound Connection ${alignr} Remote Service/Port$color
# ${tcp_portmon 32768 61000 rip 0} ${alignr} ${tcp_portmon 32768 61000 rport 0}
# ${tcp_portmon 32768 61000 rip 1} ${alignr} ${tcp_portmon 32768 61000 rport 1}
# ${tcp_portmon 32768 61000 rip 2} ${alignr} ${tcp_portmon 32768 61000 rport 2}
# ${tcp_portmon 32768 61000 rip 3} ${alignr} ${tcp_portmon 32768 61000 rport 3}
# ${tcp_portmon 32768 61000 rip 4} ${alignr} ${tcp_portmon 32768 61000 rport 4}
# ${tcp_portmon 32768 61000 rip 5} ${alignr} ${tcp_portmon 32768 61000 rport 5}
# ${tcp_portmon 32768 61000 rip 6} ${alignr} ${tcp_portmon 32768 61000 rport 6}
# ${tcp_portmon 32768 61000 rip 7} ${alignr} ${tcp_portmon 32768 61000 rport 7}
# ${tcp_portmon 32768 61000 rip 8} ${alignr} ${tcp_portmon 32768 61000 rport 8}
# ${tcp_portmon 32768 61000 rip 9} ${alignr} ${tcp_portmon 32768 61000 rport 9}
# ${tcp_portmon 32768 61000 rhost 9} ${alignr} ${tcp_portmon 32768 61000 rservice 9}
$stippled_hr
${color #ddaa00}Outbound Connection ${alignr} Remote Service/Port$color
 ${tcp_portmon 32768 61000 rhost 0} ${alignr} ${tcp_portmon 32768 61000 rport 0}
 ${tcp_portmon 32768 61000 rhost 1} ${alignr} ${tcp_portmon 32768 61000 rport 1}
 ${tcp_portmon 32768 61000 rhost 2} ${alignr} ${tcp_portmon 32768 61000 rport 2}
 ${tcp_portmon 32768 61000 rhost 3} ${alignr} ${tcp_portmon 32768 61000 rport 3}
 ${tcp_portmon 32768 61000 rhost 4} ${alignr} ${tcp_portmon 32768 61000 rport 4}
 ${tcp_portmon 32768 61000 rhost 5} ${alignr} ${tcp_portmon 32768 61000 rport 5}
 ${tcp_portmon 32768 61000 rhost 6} ${alignr} ${tcp_portmon 32768 61000 rport 6}
 ${tcp_portmon 32768 61000 rhost 7} ${alignr} ${tcp_portmon 32768 61000 rport 7}
 ${tcp_portmon 32768 61000 rhost 8} ${alignr} ${tcp_portmon 32768 61000 rport 8}
 ${tcp_portmon 32768 61000 rhost 9} ${alignr} ${tcp_portmon 32768 61000 rport 9}
${color #ddaa00}Port(s)${alignr}#Connections   
$color Inbound: ${tcp_portmon 1 32767 count}  Outbound: ${tcp_portmon 32768 61000 count}${alignr}ALL: ${tcp_portmon 1 65535 count}
${color #ddaa00}Inbound Connection ${alignr} Local Service/Port$color
 ${tcp_portmon 1 32767 rhost 0} ${alignr} ${tcp_portmon 1 32767 lservice 0}
 ${tcp_portmon 1 32767 rhost 1} ${alignr} ${tcp_portmon 1 32767 lservice 1}
# ${tcp_portmon 1 32767 rhost 2} ${alignr} ${tcp_portmon 1 32767 lservice 2}
# ${tcp_portmon 1 32767 rhost 3} ${alignr} ${tcp_portmon 1 32767 lservice 3}
# ${tcp_portmon 1 32767 rhost 4} ${alignr} ${tcp_portmon 1 32767 lservice 4}
# ${tcp_portmon 1 32767 rhost 5} ${alignr} ${tcp_portmon 1 32767 lservice 5}
#s${color lightgrey}File systems:
# / $color${df_used /}/${fs_size /} ${fs_bar /}
