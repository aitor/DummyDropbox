= DummyDropbox

http://farm5.static.flickr.com/4136/4925714505_3a3a0a6134_o.jpg

<b>I can image a Dropbox session, just for testing.</b>

Very simple library for mocking the (dropbox ruby gem)[http://rubygems.org/gems/dropbox].

So you can test your application without making real calls to Dropbox API.


== Install

    $ [sudo] gem install dummy_dropbox


== Usage

    require 'dummy_dropbox'
    
    # Optional:
    # Point where your local folder structure is located.
    # It will be used as if the real Dropbox structure was been reading.
    DropboxDummy.root_path = <your_local_folder> 
    
    session = Dropbox::Session.new('key', 'secret')
    assert_equal( File.read( "<your_local_folder>/file1.txt" ) , @session.download( '/file1.txt' ) )
    
See the *test* folder.


== TODO

The status of this dummy implementation is not very much completed, I just implemented enough for my proposes.


== Credits

Author:: Fernando Guillen: http://fernandoguillen.info
Copyright:: Copyright (c) 2010 Fernando Guillen
License:: Released under the MIT license.