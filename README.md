dubbo-extension
===============

Dubbo extension points implementation

<p>Simple tutorial:</p>

<pre><code>
<dubbo:provider serialization="cryo" />
</code></pre>

<p>Custom Kryo instance:</p>
<pre><code>
KryoRegister.register(new KryoCustom() {
	@Override
	public void custom(Kryo kryo) {
		kryo.register(Map.class, new HashMapSerializer());
		kryo.register(List.class, new ArrayListSerializer());
	}
});
</code></pre>
