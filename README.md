I have a problem with ProtocolLib                                                                                                                                        
i m using aternos host


handle=562980018192385
      memory=java.nio.DirectByteBuffer[pos=0 lim=4194304 cap=4194304]
      offset=8224
      length=26
      maxLength=32
      cache=io.netty.buffer.PoolThreadCache@32bf2abf
      tmpNioBuf=<null>
      allocator=PooledByteBufAllocator(directByDefault: true)
      refCnt=2
      readerIndex=26
      writerIndex=26
      markedReaderIndex=0
      markedWriterIndex=0
      maxCapacity=2147483647
    ]
    manager:
      com.comphenix.protocol.injector.PacketFilterManager@7f00677b[
        unhookTask=com.comphenix.protocol.injector.DelayedSingleTask@1b4ffc1a
        packetListeners=[PacketAdapter[plugin=Orebfuscator, sending=ListeningWhitelist[priority=NORMAL, packets=[UNLOAD_CHUNK[class=PacketPlayOutUnloadChunk, id=29]], gamephase=PLAYING, options=[]], receiving=EMPTY_WHITELIST], com.comphenix.protocol.async.NullPacketListener@63e1cebd]
        packetInjector=com.comphenix.protocol.injector.netty.ProtocolInjector$5@4b1358e2
        playerInjection=com.comphenix.protocol.injector.netty.ProtocolInjector$4@14d2412c
        inputBufferedPackets=[]
        recievedListeners=com.comphenix.protocol.injector.SortedPacketListenerList@6815d772
        sendingListeners=com.comphenix.protocol.injector.SortedPacketListenerList@cde5946
        hasClosed=false
        classLoader=org.bukkit.plugin.java.PluginClassLoader@4a5c94df
        reporter=com.comphenix.protocol.ProtocolLib$1@5d5bc477
        server=CraftServer{serverName=CraftBukkit,serverVersion=3553-Spigot-14a2382-ef09464,minecraftVersion=1.19}
        library=ProtocolLib v4.8.0
        asyncFilterManager=com.comphenix.protocol.async.AsyncFilterManager@5b8635d1
        knowsServerPackets=true
        knowsClientPackets=true
        phaseLoginCount=0
        phasePlayingCount=2
        packetCreation=false
        nettyInjector=com.comphenix.protocol.injector.netty.ProtocolInjector@abd381e
        pluginVerifier=com.comphenix.protocol.injector.PluginVerifier@61040caa
        hasRecycleDistance=true
        minecraftVersion=(MC: 1.19.0)
        debug=false
      ]
  Sender:
    com.comphenix.protocol.injector.netty.ChannelInjector@278e4505[
      decodeBuffer=protected void net.minecraft.network.PacketDecoder.decode(io.netty.channel.ChannelHandlerContext,io.netty.buffer.ByteBuf,java.util.List) throws java.lang.Exception
      encodeBuffer=protected void net.minecraft.network.PacketEncoder.encode(io.netty.channel.ChannelHandlerContext,java.lang.Object,io.netty.buffer.ByteBuf) throws java.lang.Exception
      factory=com.comphenix.protocol.injector.netty.InjectionFactory@3ae7ec40
      player=CraftPlayer{name=Taka_Yoko}
      updated=<null>
      playerName=<null>
      playerConnection=<null>
      networkManager=net.minecraft.network.NetworkManager@629a2035
      originalChannel=[id: 0x68833817, L:/172.20.0.10:35886 - R:/213.162.73.206:54709]
      channelField=VolatileField [accessor=DefaultFieldAccessor [field=public io.netty.channel.Channel net.minecraft.network.NetworkManager.m], container=net.minecraft.network.NetworkManager@629a2035, previous=[id: 0x68833817, L:/172.20.0.10:35886 - R:/213.162.73.206:54709], current=com.comphenix.protocol.injector.netty.ChannelInjector$3@18d96803, previousLoaded=true, currentSet=true, forceAccess=true]
      packetMarker={}
      currentEvent=<null>
      finalEvent=<null>
      unfilteredProcessedPackets=com.comphenix.protocol.injector.netty.PacketFilterQueue@4d2aa070
      vanillaDecoder=net.minecraft.network.PacketDecoder@2be1ba01
      vanillaEncoder=net.minecraft.network.PacketEncoder@5a8b782a
      finishQueue=[]
      channelListener=com.comphenix.protocol.injector.netty.ProtocolInjector@abd381e
      processor=com.comphenix.protocol.injector.NetworkProcessor@5b36c8a8
      injected=true
      closed=false
      cumulation=PooledUnsafeDirectByteBuf(ridx: 26, widx: 26, cap: 26)
      cumulator=io.netty.handler.codec.ByteToMessageDecoder$1@62400724
      singleDecode=false
      first=true
      firedChannelRead=false
      selfFiredChannelRead=true
      decodeState=1
      discardAfterReads=16
      numReads=0
      added=true
    ]
  Version:
    ProtocolLib v4.8.0
  Java Version:
    17.0.2
  Server:
    3553-Spigot-14a2382-ef09464 (MC: 1.19)

[18:30:18] [Netty Epoll Server IO #3/INFO]: Error Unable to intercept a read client packet. (java.lang.IllegalArgumentException: Unable to find a field null with the type com.mojang.authlib.GameProfile in net.minecraft.network.protocol.login.PacketLoginInStart) occured in com.comphenix.protocol.injector.netty.ChannelInjector@278e4505.
[18:30:18] [Netty Epoll Server IO #3/ERROR]:   [ProtocolLib] INTERNAL ERROR: Unable to intercept a read client packet.
  If this problem hasn't already been reported, please open a ticket
  at https://github.com/dmulloy2/ProtocolLib/issues with the following data:
  Stack Trace:
  java.lang.IllegalArgumentException: Unable to find a field null with the type com.mojang.authlib.GameProfile in net.minecraft.network.protocol.login.PacketLoginInStart
  	at com.comphenix.protocol.reflect.FuzzyReflection.getFieldByType(FuzzyReflection.java:397)
  	at com.comphenix.protocol.reflect.accessors.Accessors.getFieldAccessor(Accessors.java:57)
  	at com.comphenix.protocol.injector.netty.ChannelInjector.handleLogin(ChannelInjector.java:658)
  	at com.comphenix.protocol.injector.netty.ChannelInjector.decode(ChannelInjector.java:591)
  	at io.netty.handler.codec.ByteToMessageDecoder.decodeRemovalReentryProtection(ByteToMessageDecoder.java:510)
  	at io.netty.handler.codec.ByteToMessageDecoder.callDecode(ByteToMessageDecoder.java:449)
  	at io.netty.handler.codec.ByteToMessageDecoder.channelRead(ByteToMessageDecoder.java:279)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at com.comphenix.protocol.injector.netty.ChannelInjector$2.channelRead(ChannelInjector.java:292)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.handler.codec.ByteToMessageDecoder.fireChannelRead(ByteToMessageDecoder.java:327)
  	at io.netty.handler.codec.ByteToMessageDecoder.channelRead(ByteToMessageDecoder.java:299)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.handler.codec.ByteToMessageDecoder.fireChannelRead(ByteToMessageDecoder.java:327)
  	at io.netty.handler.codec.ByteToMessageDecoder.channelRead(ByteToMessageDecoder.java:299)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.handler.timeout.IdleStateHandler.channelRead(IdleStateHandler.java:286)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.channel.DefaultChannelPipeline$HeadContext.channelRead(DefaultChannelPipeline.java:1410)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.DefaultChannelPipeline.fireChannelRead(DefaultChannelPipeline.java:919)
  	at io.netty.channel.epoll.AbstractEpollStreamChannel$EpollStreamUnsafe.epollInReady(AbstractEpollStreamChannel.java:800)
  	at io.netty.channel.epoll.EpollEventLoop.processReady(EpollEventLoop.java:487)
  	at io.netty.channel.epoll.EpollEventLoop.run(EpollEventLoop.java:385)
  	at io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:995)
  	at io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
  	at java.base/java.lang.Thread.run(Thread.java:833)
  Dump:
  Parameters: 
    io.netty.buffer.PooledUnsafeDirectByteBuf@3e1cc442[
      memoryAddress=140037828112432
      recyclerHandle=io.netty.util.Recycler$DefaultHandle@55039154
      chunk=Chunk(4a2b49f5: 16%, 655360/4194304)
      handle=562980018192385
      memory=java.nio.DirectByteBuffer[pos=0 lim=4194304 cap=4194304]
      offset=8224
      length=26
      maxLength=32
      cache=io.netty.buffer.PoolThreadCache@32bf2abf
      tmpNioBuf=<null>
      allocator=PooledByteBufAllocator(directByDefault: true)
      refCnt=2
      readerIndex=26
      writerIndex=26
      markedReaderIndex=0
      markedWriterIndex=0
      maxCapacity=2147483647
    ]
    manager:
      com.comphenix.protocol.injector.PacketFilterManager@7f00677b[
        unhookTask=com.comphenix.protocol.injector.DelayedSingleTask@1b4ffc1a
        packetListeners=[PacketAdapter[plugin=Orebfuscator, sending=ListeningWhitelist[priority=NORMAL, packets=[UNLOAD_CHUNK[class=PacketPlayOutUnloadChunk, id=29]], gamephase=PLAYING, options=[]], receiving=EMPTY_WHITELIST], com.comphenix.protocol.async.NullPacketListener@63e1cebd]
        packetInjector=com.comphenix.protocol.injector.netty.ProtocolInjector$5@4b1358e2
        playerInjection=com.comphenix.protocol.injector.netty.ProtocolInjector$4@14d2412c
        inputBufferedPackets=[]
        recievedListeners=com.comphenix.protocol.injector.SortedPacketListenerList@6815d772
        sendingListeners=com.comphenix.protocol.injector.SortedPacketListenerList@cde5946
        hasClosed=false
        classLoader=org.bukkit.plugin.java.PluginClassLoader@4a5c94df
        reporter=com.comphenix.protocol.ProtocolLib$1@5d5bc477
        server=CraftServer{serverName=CraftBukkit,serverVersion=3553-Spigot-14a2382-ef09464,minecraftVersion=1.19}
        library=ProtocolLib v4.8.0
        asyncFilterManager=com.comphenix.protocol.async.AsyncFilterManager@5b8635d1
        knowsServerPackets=true
        knowsClientPackets=true
        phaseLoginCount=0
        phasePlayingCount=2
        packetCreation=false
        nettyInjector=com.comphenix.protocol.injector.netty.ProtocolInjector@abd381e
        pluginVerifier=com.comphenix.protocol.injector.PluginVerifier@61040caa
        hasRecycleDistance=true
        minecraftVersion=(MC: 1.19.0)
        debug=false
      ]
  Sender:
    com.comphenix.protocol.injector.netty.ChannelInjector@278e4505[
      decodeBuffer=protected void net.minecraft.network.PacketDecoder.decode(io.netty.channel.ChannelHandlerContext,io.netty.buffer.ByteBuf,java.util.List) throws java.lang.Exception
      encodeBuffer=protected void net.minecraft.network.PacketEncoder.encode(io.netty.channel.ChannelHandlerContext,java.lang.Object,io.netty.buffer.ByteBuf) throws java.lang.Exception
      factory=com.comphenix.protocol.injector.netty.InjectionFactory@3ae7ec40
      player=CraftPlayer{name=Taka_Yoko}
      updated=<null>
      playerName=<null>
      playerConnection=<null>
      networkManager=net.minecraft.network.NetworkManager@629a2035
      originalChannel=[id: 0x68833817, L:/172.20.0.10:35886 - R:/213.162.73.206:54709]
      channelField=VolatileField [accessor=DefaultFieldAccessor [field=public io.netty.channel.Channel net.minecraft.network.NetworkManager.m], container=net.minecraft.network.NetworkManager@629a2035, previous=[id: 0x68833817, L:/172.20.0.10:35886 - R:/213.162.73.206:54709], current=com.comphenix.protocol.injector.netty.ChannelInjector$3@18d96803, previousLoaded=true, currentSet=true, forceAccess=true]
      packetMarker={}
      currentEvent=<null>
      finalEvent=<null>
      unfilteredProcessedPackets=com.comphenix.protocol.injector.netty.PacketFilterQueue@4d2aa070
      vanillaDecoder=net.minecraft.network.PacketDecoder@2be1ba01
      vanillaEncoder=net.minecraft.network.PacketEncoder@5a8b782a
      finishQueue=[]
      channelListener=com.comphenix.protocol.injector.netty.ProtocolInjector@abd381e
      processor=com.comphenix.protocol.injector.NetworkProcessor@5b36c8a8
      injected=true
      closed=false
      cumulation=PooledUnsafeDirectByteBuf(ridx: 26, widx: 26, cap: 26)
      cumulator=io.netty.handler.codec.ByteToMessageDecoder$1@62400724
      singleDecode=false
      first=true
      firedChannelRead=false
      selfFiredChannelRead=true
      decodeState=1
      discardAfterReads=16
      numReads=0
      added=true
    ]
  Version:
    ProtocolLib v4.8.0
  Java Version:
    17.0.2
  Server:
    3553-Spigot-14a2382-ef09464 (MC: 1.19)

[18:30:19] [Netty Epoll Server IO #3/INFO]: Error Unable to intercept a read client packet. (java.lang.IllegalArgumentException: Unable to find a field null with the type com.mojang.authlib.GameProfile in net.minecraft.network.protocol.login.PacketLoginInStart) occured in com.comphenix.protocol.injector.netty.ChannelInjector@278e4505.
[18:30:19] [Netty Epoll Server IO #3/ERROR]:   [ProtocolLib] INTERNAL ERROR: Unable to intercept a read client packet.
  If this problem hasn't already been reported, please open a ticket
  at https://github.com/dmulloy2/ProtocolLib/issues with the following data:
  Stack Trace:
  java.lang.IllegalArgumentException: Unable to find a field null with the type com.mojang.authlib.GameProfile in net.minecraft.network.protocol.login.PacketLoginInStart
  	at com.comphenix.protocol.reflect.FuzzyReflection.getFieldByType(FuzzyReflection.java:397)
  	at com.comphenix.protocol.reflect.accessors.Accessors.getFieldAccessor(Accessors.java:57)
  	at com.comphenix.protocol.injector.netty.ChannelInjector.handleLogin(ChannelInjector.java:658)
  	at com.comphenix.protocol.injector.netty.ChannelInjector.decode(ChannelInjector.java:591)
  	at io.netty.handler.codec.ByteToMessageDecoder.decodeRemovalReentryProtection(ByteToMessageDecoder.java:510)
  	at io.netty.handler.codec.ByteToMessageDecoder.callDecode(ByteToMessageDecoder.java:449)
  	at io.netty.handler.codec.ByteToMessageDecoder.channelRead(ByteToMessageDecoder.java:279)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at com.comphenix.protocol.injector.netty.ChannelInjector$2.channelRead(ChannelInjector.java:292)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.handler.codec.ByteToMessageDecoder.fireChannelRead(ByteToMessageDecoder.java:327)
  	at io.netty.handler.codec.ByteToMessageDecoder.channelRead(ByteToMessageDecoder.java:299)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.handler.codec.ByteToMessageDecoder.fireChannelRead(ByteToMessageDecoder.java:327)
  	at io.netty.handler.codec.ByteToMessageDecoder.channelRead(ByteToMessageDecoder.java:299)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.handler.timeout.IdleStateHandler.channelRead(IdleStateHandler.java:286)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.AbstractChannelHandlerContext.fireChannelRead(AbstractChannelHandlerContext.java:357)
  	at io.netty.channel.DefaultChannelPipeline$HeadContext.channelRead(DefaultChannelPipeline.java:1410)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:379)
  	at io.netty.channel.AbstractChannelHandlerContext.invokeChannelRead(AbstractChannelHandlerContext.java:365)
  	at io.netty.channel.DefaultChannelPipeline.fireChannelRead(DefaultChannelPipeline.java:919)
  	at io.netty.channel.epoll.AbstractEpollStreamChannel$EpollStreamUnsafe.epollInReady(AbstractEpollStreamChannel.java:800)
  	at io.netty.channel.epoll.EpollEventLoop.processReady(EpollEventLoop.java:487)
  	at io.netty.channel.epoll.EpollEventLoop.run(EpollEventLoop.java:385)
  	at io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:995)
  	at io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
  	at java.base/java.lang.Thread.run(Thread.java:833)
  Dump:
  Parameters: 
    io.netty.buffer.PooledUnsafeDirectByteBuf@35f97af6[
      memoryAddress=140037828112432
      recyclerHandle=io.netty.util.Recycler$DefaultHandle@6d1f86df
      chunk=Chunk(4a2b49f5: 16%, 655360/4194304)
      handle=562980018192385
      memory=java.nio.DirectByteBuffer[pos=0 lim=4194304 cap=4194304]
      offset=8224
      length=26
      maxLength=32
      cache=io.netty.buffer.PoolThreadCache@32bf2abf
      tmpNioBuf=<null>
      allocator=PooledByteBufAllocator(directByDefault: true)
      refCnt=2
      readerIndex=26
      writerIndex=26
      markedReaderIndex=0
      markedWriterIndex=0
      maxCapacity=2147483647
    ]
    manager:
      com.comphenix.protocol.injector.PacketFilterManager@7f00677b[
        unhookTask=com.comphenix.protocol.injector.DelayedSingleTask@1b4ffc1a
        packetListeners=[PacketAdapter[plugin=Orebfuscator, sending=ListeningWhitelist[priority=NORMAL, packets=[UNLOAD_CHUNK[class=PacketPlayOutUnloadChunk, id=29]], gamephase=PLAYING, options=[]], receiving=EMPTY_WHITELIST], com.comphenix.protocol.async.NullPacketListener@63e1cebd]
        packetInjector=com.comphenix.protocol.injector.netty.ProtocolInjector$5@4b1358e2
        playerInjection=com.comphenix.protocol.injector.netty.ProtocolInjector$4@14d2412c
        inputBufferedPackets=[]
        recievedListeners=com.comphenix.protocol.injector.SortedPacketListenerList@6815d772
        sendingListeners=com.comphenix.protocol.injector.SortedPacketListenerList@cde5946
        hasClosed=false
        classLoader=org.bukkit.plugin.java.PluginClassLoader@4a5c94df
        reporter=com.comphenix.protocol.ProtocolLib$1@5d5bc477
        server=CraftServer{serverName=CraftBukkit,serverVersion=3553-Spigot-14a2382-ef09464,minecraftVersion=1.19}
        library=ProtocolLib v4.8.0
        asyncFilterManager=com.comphenix.protocol.async.AsyncFilterManager@5b8635d1
        knowsServerPackets=true
        knowsClientPackets=true
        phaseLoginCount=0
        phasePlayingCount=2
        packetCreation=false
        nettyInjector=com.comphenix.protocol.injector.netty.ProtocolInjector@abd381e
        pluginVerifier=com.comphenix.protocol.injector.PluginVerifier@61040caa
        hasRecycleDistance=true
        minecraftVersion=(MC: 1.19.0)
        debug=false
      ]
  Sender:
    com.comphenix.protocol.injector.netty.ChannelInjector@278e4505[
      decodeBuffer=protected void net.minecraft.network.PacketDecoder.decode(io.netty.channel.ChannelHandlerContext,io.netty.buffer.ByteBuf,java.util.List) throws java.lang.Exception
      encodeBuffer=protected void net.minecraft.network.PacketEncoder.encode(io.netty.channel.ChannelHandlerContext,java.lang.Object,io.netty.buffer.ByteBuf) throws java.lang.Exception
      factory=com.comphenix.protocol.injector.netty.InjectionFactory@3ae7ec40
      player=CraftPlayer{name=Taka_Yoko}
      updated=<null>
      playerName=<null>
      playerConnection=<null>
      networkManager=net.minecraft.network.NetworkManager@629a2035
      originalChannel=[id: 0x68833817, L:/172.20.0.10:35886 - R:/213.162.73.206:54709]
      channelField=VolatileField [accessor=DefaultFieldAccessor [field=public io.netty.channel.Channel net.minecraft.network.NetworkManager.m], container=net.minecraft.network.NetworkManager@629a2035, previous=[id: 0x68833817, L:/172.20.0.10:35886 - R:/213.162.73.206:54709], current=com.comphenix.protocol.injector.netty.ChannelInjector$3@18d96803, previousLoaded=true, currentSet=true, forceAccess=true]
      packetMarker={}
      currentEvent=<null>
      finalEvent=<null>
      unfilteredProcessedPackets=com.comphenix.protocol.injector.netty.PacketFilterQueue@4d2aa070
      vanillaDecoder=net.minecraft.network.PacketDecoder@2be1ba01
      vanillaEncoder=net.minecraft.network.PacketEncoder@5a8b782a
      finishQueue=[]
      channelListener=com.comphenix.protocol.injector.netty.ProtocolInjector@abd381e
      processor=com.comphenix.protocol.injector.NetworkProcessor@5b36c8a8
      injected=true
      closed=false
      cumulation=PooledUnsafeDirectByteBuf(ridx: 26, widx: 26, cap: 26)
      cumulator=io.netty.handler.codec.ByteToMessageDecoder$1@62400724
      singleDecode=false
      first=true
      firedChannelRead=false
      selfFiredChannelRead=true
      decodeState=1
      discardAfterReads=16
      numReads=0
      added=true
    ]
  Version:
    ProtocolLib v4.8.0
  Java Version:
    17.0.2
  Server:
    3553-Spigot-14a2382-ef09464 (MC: 1.19)
