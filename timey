#!/usr/bin/python 

from gi.repository import Gtk, GLib
from gi.repository import AppIndicator3 as a
from datetime import datetime as e

def update(b):
  b.set_label(e.now().strftime("%H:%M"), "Time")
  return True

c = Gtk.MenuItem("Quit")
c.connect("activate", Gtk.main_quit, "text")
c.show()

d = Gtk.Menu()
d.append(c)

b = a.Indicator.new("time","user-idle-panel", a.IndicatorCategory.APPLICATION_STATUS)
b.set_status(a.IndicatorStatus.ACTIVE)
b.set_menu(d)
update(b)

GLib.timeout_add_seconds(60, update, b)

Gtk.main()

