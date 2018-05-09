<html>

<div align="center">
<font face="cambria">
<p><a target="_blank" href="images/TrustNote-Logo.png"><img align="center" width="300px" height="300px" src="images/TrustNote-Logo.png"></a></p>

<p><b><font size="5">FAST ∙ SCALABLE ∙ DEVELOPER FRIENDLY</font></b></p>

<p><b><font size="5">TrustNote Cryptographic Algorithms</font></b></p>

<p><b><font >TrustNote Institute of Technology</font></b></p>
<p><font >May 2018</font></p>

</div>

<hr>

<div align="justify">
<font face="cambria" >

 <h1><b>Disclaimer</b></h1>
<p>TrustNote Institute of Technology and Research & Development section hereby declare that, this package is under MIT open source software license and this software is distributed without any warranty. TrustNote Institute of Technology declares that we are NOT responsible for direct, indirect, incidental or consequential damages resulting from any defect, error or failure to perform. This package is experimental and a work-in-progress, use at your own risk. TrustNote R&D team can update (add/remove packages) any time without informing the users.</P>

<h1><b>Contact Us</b></h1>
<ul>
<li><p>Business Enquiries:  <a href="foundation@trustnote.org" target="_blank" rel="external">foundation@trustnote.org</a></p></li>
<li><p>Technical Support:  <a href="community@trustnote.org" target="_blank" rel="external">community@trustnote.org</a></p></li>
</ul>

<h1><b>Copyright</b></h1>
<p>© 2018 TrustNote Institute of Technology. All rights reserved.</p>

</font>
</div>

<hr>

<div id="toc_container" align="left">
<font face="cambria" >

<h1><b>Contents</b></h1>
<ul class="toc_list">
  <p><a href="#How-do-we-select-the-best-among-nominees">1. How do we select the best among nominees?</a></p>
     <ul><p><a href="#Why-Blake2">1.1. Why Blake2?</a></p>
         <p><a href="#Why-Ed25519">1.2. Why Ed25519?</a></p>
         <p><a href="#Why-Equihash">1.3. Why Equihash?</a></p></ul>
  <p><a href="#Introduction-&-Mathematical-foundation">2. Introduction & Mathematical foundation</a></p>
     <ul><p><a href="#Blake2">2.1. Blake2</a></p>
             <ul><p><a href="#Blake2b">2.1.1. Blake2b</a></p>
             <p><a href="#Blake2s">2.1.2. Blake2s</a></p></ul>
         <p><a href="#Ed25519">2.2. Ed25519</a></p>
         <p><a href="#Equihash">2.3. Equihash</a></p></ul>
  <p><a href="#How-to-get-started-with-it">3. How to get started with it?</a></p>
     <ul><p><a href="#Lets-get-started-with-Blake2-Node-js-Addon">3.1. Let's get started with Blake2-Node.js-Addon</a></p>
             <ul><p><a href="#Blake2-Pure-JavaScript-Node-Addon">3.1.1. Blake2 Pure JavaScript-Node-Addon</a></p>
             <p><a href="#Blake2-C-Node-Addon">3.1.2. Blake2 C/C++ Node-Addon</a></p></ul>
         <p><a href="#Lets-get-started-with-Ed25519-Node-Addon">3.2. Let's get started with Ed25519-Node-Addon</a></p>
         <p><a href="#Lets-get-started-with-Equihash">3.3. Let's get started with Equihash</a></p></ul>
  <p><a href="#Discussion">4. Discussion</a></p>
  <p><a href="#References">5. References</a></p>

</ul>
</font>
</div>

<hr>

<div align="justify">
<font face="cambria" >

<h1><a id="How-do-we-select-the-best-among-nominees"></a>1. How do we select the best among nominees?</h1>

<p>Selecting an efficient algorithm which also would be robust and secure while it can be performed very fast for many times per second on variety of devices is a very important and difficult process. Any failure or security hole will result in an irreparable damage. TrustNote Institute of Technology - R&D section criteria for selecting its project's cryptographic algorithms are:</p>

<ul>
  <li> High security level and Robustness </li>
  <li> Better performance</li>
  <li> Most compatible one with variety of devices</li>
</ul>

<p>So, any algorithm fits the best into these three criteria will be selected by R&D section. But it's not the end, after selecting the best available algorithm, experts in TrustNote will perform several challenging tests to verify it’s trustworthy.</p>

<h2><a id="Why-Blake2"></a>1.1. Why Blake2?</h2>

<p>Selecting an efficient, secure and fast hash function is crucial during the design process of any cryptocurrency infrastructure. A proper hash function algorithm has enough robustness so in case of encountering Collision attack, Preimage attack and etc. It should be undefeatable. A list of available hash functions presented in the table below:</p>

</font>
</div>

<div align="center">
<font face="cambria" >

 <table>
   <TR ALIGN="CENTER">
      <TH COLSPAN="3">Cryptographic hash functions</TH>
   </TR>
   <TR ALIGN="CENTER">
      <TD>HAVAL</TD>
      <TD>MD5</TD>
      <TD>JH</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>SHA-1</TD>
      <TD>Skein</TD>
      <TD>MD2</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>SHA-2</TH>
      <TD>LM hash</TD>
      <TD>Keccak</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>SHA-3</TD>
      <TD>CubeHash</TD>
      <TD>MD4</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>BLAKE2</TD>
      <TD>ECOH</TD>
      <TD>MD6</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>BLAKE</TD>
      <TD>ECOH</TD>
      <TD>MDC-2</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>Grøstl</TD>
      <TD>FSB</TD>
      <TD>Data 2</TD>
   </TR>
</TABLE>

</div>

<div align="justify">
<font face="cambria" >

<p>Please, note that: The orders in table above are totally by randomness and this table is not sorted by any kind of factors.</p>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Hash function Supercup.png"><img align="center" src="images/TrustNote-TR-01-Hash function Supercup.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >

<p>A full list of available Hash functions’ eBASH (ECRYPT Benchmarking of All Submitted Hashes) benchmarks available at:</p>

<ul>
 <li>eBASH benchmarks for <a href="http://bench.cr.yp.to/impl-hash/blake2b.html" target="_blank" rel="external">Blake2b</a>.</li>
 <li>eBASH benchmarks for <a href="http://bench.cr.yp.to/impl-hash/blake2s.html" target="_blank" rel="external">Blake2s</a>.</li>
 <li>eBASH benchmarks for <a href="http://bench.cr.yp.to/results-hash.html" target="_blank" rel="external">results of benchmarking of all hash functions</a>.</li>
 <li>eBASH benchmarks for <a href="http://bench.cr.yp.to/primitives-hash.html" target="_blank" rel="external">full list of hash functions</a>.</li>
</ul>

<p>However, this is not the main reason for choosing Blake2. In the rest of this section, the primary reasons of selecting Blake2 among plenty of available hash functions will be explained.</p>

<p>BLAKE2 is a cryptographic hash function faster than MD5, SHA-1, SHA-2, and SHA-3, yet is at least as secure as the latest standard SHA-3. BLAKE2 has been adopted by many projects due to its high speed, security, and simplicity. BLAKE2 comes in two types (Aumasson , Neves , Wilcox-O'Hearn, & Winnerlein , 2017)</p>

<ul>
<li><p><b>BLAKE2b</b> (or just BLAKE2) is optimized for 64-bit platforms including NEON-enabled ARMs and produces digests of any size between 1 and 64 bytes.</p></li>
<li><p><b>BLAKE2s</b> is optimized for 8- to 32-bit platforms and produces digests of any size between 1 and 32 bytes.</p></li>
</ul>
<p>BLAKE2 includes the 4-way parallel BLAKE2bp and 8-way parallel BLAKE2sp designed for increased performance on multicore or SIMD (Single Instruction, Multiple Data) CPUs. BLAKE2 offers these algorithms tuned to your specific requirements, such as keyed hashing (that is, MAC or PRF), hashing with a salt, updatable or incremental tree-hashing, or any combination thereof (Aumasson , Neves , Wilcox-O'Hearn, & Winnerlein , 2017).</p>


<p>The SHA-3 Competition succeeded in selecting a hash function that complements SHA-2 and is much faster than SHA-2 in hardware (Chang, et al., 2012). There is nevertheless a demand for fast software hashing for applications such as integrity checking and deduplication in file systems and etc. (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013)</p>

<p>The chart below is the speed comparison of various popular hash functions, taken from eBACS’s “sandy” measurements. SHA-3 and BLAKE2 have no known security issues. SHA-1, MD5, SHA-256, and SHA-512 are susceptible to length-extension. SHA-1 and MD5 are vulnerable to collisions. MD5 is vulnerable to chosen-prefix collisions (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013).</p>

<p>BLAKE thus appears to be a good candidate for fast software hashing. BLAKE2 aims to provide the highest security level, be it in terms of classical notions as (second) preimage or collision resistance, or of theoretical notions as pseudo randomness or undifferentiability (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013).</p>

<p>Blake2 offers the following properties and capabilities (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>

<ul>
  <li>Faster than MD5 on 64-bit Intel platforms.</li>
  <li>32% less RAM required than BLAKE.</li>
  <li>Minimal padding, which is faster and simpler to implement.</li>
  <li>Direct support, with no overhead, of:</li>
    <ul><li>Parallelism for many-times faster hashing on multicore or SIMD (Single Instruction, Multiple Data) CPUs.</li>
        <li>Tree hashing for incremental update or verification of large files.</li>
        <li>Prefix-MAC for authentication that is simpler and faster than HMAC.</li>
        <li>Personalization for defining a unique hash function for each application.</li></ul>
</ul>

<p>Consequently, it is evident that Blake2 is the best available hash function until now. We may change the hash if we find some flaw in Blake2 or if we find another hash function algorithm which offers higher assurance and performance. For more in-depth information about Blake2 capabilities, please visit the <a href="https://blake2.net/" target="_blank" rel="external">Blake2</a> official website.</p>

</font>
</div>


<div align="justify">
<font face="cambria" >

<h2><a id="Why-Ed25519"></a>1.2. Why Ed25519?</h2>

<p>In previous section the importance and challenges of selecting a cryptographic hash function discussed carefully. In this a Public-key cryptography algorithm will be selected. There are plenty of theories that these algorithms are developed and created based on them such as: Discrete logarithm, Elliptic-curve cryptography, Non-commutative cryptography, RSA (Rivest–Shamir–Adleman) problem and Trapdoor function. Furthermore, for each mathematical algorithm which are already mentioned, there are numerous number of Public-key cryptography algorithms which are presented in the table below:</p>

</font>
</div>

<div ALIGN="CENTER">
<font face="cambria" >
<TABLE ALIGN="CENTER"">
   <TR>
      <TH COLSPAN="3"><H3>Public-key cryptography</H3>
      </TH>
   </TR>
   <TR ALIGN="CENTER">
      <TD>Cramer–Shoup</TD>
      <TD>ECDSA</TD>
      <TD>EdDSA</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>DH</TD>
      <TD>EKE</TD>
      <TD>Schnorr</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>DSA</TH>
      <TD>ElGamal (signature scheme)</TD>
      <TD>SPEKE</TD>
   </TR>
   <TR ALIGN="CENTER">
      <TD>ECDH</TD>
      <TD>MQV</TD>
      <TD>SRP</TD>
   </TR>
</TABLE>

</div>

<div align="justify">
<font face="cambria" >

<p>A full list of available Public-key cryptographies’ eBATS (ECRYPT Benchmarking of Asymmetric Systems) benchmarks available at:</p>

<ul>
  <li>eBATS benchmarks for <a href="http://bench.cr.yp.to/impl-sign/ed25519.html" target="_blank" rel="external">Ed25519</a>.</li>
  <li>eBATS benchmarks for <a href="http://bench.cr.yp.to/results-sign.html" target="_blank" rel="external">results of benchmarking of all Public-key signatures</a>.</li>
  <li>eBATS benchmarks for <a href="http://bench.cr.yp.to/primitives-sign.html" target="_blank" rel="external">full list of Public-key signatures</a>.</li>
</ul>

<p>However, this is not the main reason for choosing Ed25519. The graphs below are the speed comparison of popular public-key cryptography, adopted from wolfssl measurements.</p>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Sign and Verify on Raspbery Pi.png"><img align="center" src="images/TrustNote-TR-01-Sign and Verify on Raspbery Pi.png"></a></p>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Sign and Verify times.png"><img align="center" src="images/TrustNote-TR-01-Sign and Verify times.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >

<p> In the rest of this section, the primary reasons of selecting Ed25519 among plenty of available Public-key signatures will be introduced. List of Ed25519 features is presented below as the major reasons for selecting Ed25519 (Bernstein, Duif, Lange, Schwabe, & Yang, 2011).</p>

<ul>
	<li><b>Fast single-signature verification</b> Ed25519 takes only 273364 cycles to verify a signature on Intel's widely deployed Nehalem/Westmere lines of CPUs. This performance measurement is for short messages. </li>
	<li><b>Even faster batch verification</b> Ed25519 performs a batch of 64 separate signature verifications (verifying 64 signatures of 64 messages under 64 public keys) in only 8.55 million cycles, i.e., under 134000 cycles per signature. It fits easily into L1 cache, so contention between cores is negligible: a quad-core 2.4GHz Westmere verifies 71000 signatures per second, while keeping the maximum verification latency below 4 milliseconds.</li>
	<li><b>Very fast signing</b> Ed25519 takes only 87548 cycles to sign a message.</li>
	<li><b>Fast key generation</b> Key generation is almost as fast as signing. There is a slight penalty for key generation to obtain a secure random number from the operating system.</li>
	<li><b>High security level</b> This system has a 2128 security target; The best attacks known actually cost more than 2140 bit operations on average, and degrade quadratically in success probability as the number of bit operations drops. </li>
	<li><b>Foolproof session keys</b> Signatures are generated deterministically; key generation consumes new randomness but new signatures do not. This is not only a speed feature but also a security feature, directly relevant to the recent collapse of the Sony PlayStation 3 security system. </li>
	<li><b>Collision resilience</b> Hash-function collisions do not break this system. This adds a layer of defense against the possibility of weakness in the selected hash function.</li>
	<li><b>No secret array indices</b> Ed25519 never reads or writes data from secret addresses in RAM; the pattern of addresses is completely predictable. The software is therefore immune to cache-timing attacks, hyper threading attacks, and other side-channel attacks that rely on leakage of addresses through the CPU cache.</li>
	<li><b>No secret branch conditions</b> Ed25519 never performs conditional branches based on secret data; the pattern of jumps is completely predictable. The software is therefore immune to side-channel attacks that rely on leakage of information through the branch-prediction unit.</li>
	<li><b>Small signatures</b> Signatures fit into 64 bytes. These signatures are actually compressed versions of longer signatures; the times for compression and decompression are included in the cycle counts reported above.</li>
	<li><b>Small keys </b> Public keys consume only 32 bytes. The times for compression and decompression are again included.</li>
</ul>

<h3>BIP32-Ed25519</h3>

<h4>A. Setup</h4>

<p>Ed25519 is described in (Bernstein, Duif, Lange, Schwabe, & Yang, 2011) and is a part of an IETF draft in (Josefsson & Liusvaara, Edwards-curve digital signature algorithm, 2016).</p>

<p>The coordinates (x,y) are pairs of elements of the prime field F<sub>p</sub>, where p = 2<sup>255</sup> - 19. The base point B has a base order n of 2<sup>252</sup> + 27742317777372353535851937790883648493. The infinity point is (0,0) and the identity point is (0,1).</p>

<h4>B. Keys and signature</h4>

<p>The private key &Atilde; is a 32-byte cryptographically-secure random value. The public key A is derived as follows:</p>

<ul>
	<p>1. Let H512() be SHA512. Hash the 32-byte private key &Atilde; using H512, storing the digest in a 64-byte buffer, denoted k. We call k an extended private key. Split k into the lower 32 bytes k<sub>L</sub> and upper 32 bytes k<sub>R</sub>.</p>
	<p>2. Modify k<sub>L</sub>: the lowest 3 bits of the first byte of are cleared, the highest bit of the last byte is cleared, and the second highest bit of the last byte is set.</p>
	<p>3. Interpret k<sub>L</sub> as a little-endian integer and perform a fixed-base scalar multiplication [k<sub>L</sub>]B.</p>
	<p>4. The public key A is the encoding of the point [k<sub>L</sub>]B as follows. First encode the y coordinate (in the range <math>0 &le; y < p </math>) as a little-endian string of 32 octets. The most significant bit of the final octet is always zero. To form the encoding of the point [k<sub>L</sub>]B, copy the least significant bit of the x coordinate to the most significant bit of the final octet. The result is the public key.</p>
</ul>

<p>Signature for message M is produced as follows:</p>

<ul>
	<p>1. Compute H512(kR||M) and interpret the result as a little-endian-encoded integer r. Compute r &larr; r mod n.</p>
	<p>2. Compute point [r]B and let R be its encoding.</p>
	<p>3. Compute x &larr; H512(R||A||M), and interpret the 64-byte digest as a little-endian integer.</p>
	<p>4. Compute S = (r + x · [k<sub>L</sub>])  mod n.</p>
	<p>5. The string R||S is the signature.</p>
</ul>

<h3>BIP32-ED25519: SPECIFICATION</h3>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-BIP32-Ed25519.png"><img align="center" src="images/TrustNote-TR-01-BIP32-Ed25519.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >

<h4>A. Root keys</h4>

<p>Let &Atilde; be 256-bit master secret. Then derive k = H512(&Atilde;) and denote its left 32-byte by k<sub>L</sub> and right one by k<sub>R</sub>. If the third highest bit of the last byte of k<sub>L</sub> is not zero, discard &Atilde; Otherwise additionally set the bits in k<sub>L</sub> as follows: the lowest 3 bits of the first byte of k<sub>L</sub> of are cleared, the highest bit of the last byte is cleared, the second highest bit of the last byte is set. The resulting pair (k<sub>L</sub>,k<sub>R</sub>) is the extended root private key, and A &le; [k<sub>L</sub>]B is the root public key after encoding. Derive c ← H256(0x01||&Atilde);, where H<sub>256</sub> is SHA-256, and call it the root chain code.</p>

<h4>B. Child keys</h4>

<p>The root key can have 2<sup>32</sup> child keys indexed from 0 to 2<sup>32</sup> - 1; the first 2<sup>31</sup> of them can have their own children and so on. The procedure of child key derivation is the same for the root and its children.<p>

<p>Let c<sup>P</sup> be the chain code. Let k<sup>P</sup>  = (k<sup>P</sup><sub>L</sub>,k<sup>P</sup><sub>R</sub>) be the extended private key and A<sup>P</sup> the public key. Recall that F<sub>K</sub>  stands for HMAC-SHA512 with key K.</p>

<h4>C. Private child key</h4>

<p>Extended private key k<sub>i</sub>  = (k<sub>L</sub>,k<sub>R</sub>) for child i is produced as follows:</p>

<p>1)</p>

<p align="center">Z &larr; F<sup>P</sup><sub>c</sub>(0x02||A<sup>P</sup>||i), i < 2<sup>31</sup>;</p>
<p align="center">Z &larr; F<sup>P</sup><sub>c</sub>(0x02||k<sup>P</sup>||i), i &ge; 2<sup>31</sup>;</p>

<p>where A<sup>P</sup> is serialized as little-endian 32-byte string, k<sup>P</sup> is viewed as (k<sup>P</sup><sub>L</sub>,k<sup>P</sup><sub>R</sub>)  and both values are serialized as little-endian, and i is serialized as little-endian 4-byte string.</p>

<p>2)</p>


<p align="center">k<sub>L</sub>  &larr; < 8[Z<sub>L</sub>] + [k<sup>P</sup><sub>L</sub>] >,</p>
<p align="center">k<sub>R</sub>  &larr; <[Z<sub>R</sub>] + [k<sup>P</sup><sub>R</sub>]  mod 2<sup>256</sup>.</p>

<p>Where Z<sub>L</sub> is the left 28-byte part of  Z, and Z<sub>R</sub> is the right 32-byte part of Z. If k<sub>L</sub> is divisible by the base order n, discard the child.</p>


<p>3) The child chain code is defined as</p>

<p align="center">Z<sub>i</sub> &larr; F<sup>P</sup><sub>c</sub>(0x03||A<sup>P</sup>||i), i < 2<sup>31</sup>;</p>
<p align="center">Z<sub>i</sub> &larr; F<sup>P</sup><sub>c</sub>(0x01||K<sup>P</sup>||i), i &ge; 2<sup>31</sup>;</p>

<p>Where the output of F is truncated to the right 32 bytes. The child public key A<sub>i</sub> is derived as [A]<sub>i</sub> = [k<sub>L</sub>]B.</p>

<h4>D. Public child key</h4>

<p>Public key A<sub>i</sub> for child i is produced as follows:</p>

<p>1)</p>

<p align="center">Z &larr; F<sup>P</sup><sub>c</sub>(0x02||A<sup>P</sup>||i), i < 2<sup>31</sup>;</p>
<p align="center">Z &larr; F<sup>P</sup><sub>c</sub>(0x02||k<sup>P</sup>||i), i &ge; 2<sup>31</sup>;</p>

<p>Where A<sup>P</sup> is serialized as little-endian 32-byte string, and i is serialized as little-endian 4-byte string. Note that like in the original BIP32 the public key for i &ge; 2<sup>31</sup> can be computed only by the private key owner and those knowing the parent private key.</p>

<p>2)</p>

<p align="center">A<sub>i</sub> &larr; A<sup>P</sup> + [8Z<sub>L</sub>]B</p>

<p>where Z<sub>L</sub> is the left 28-byte part of Z interpreted as 224-bit integer using the little-endian representation. If A<sub>i</sub> is the identity point (0,1), discard the child.</p>

<p>3) The child chain code is defined as</p>

<p align="center">Z<sub>i</sub> &larr; F<sup>P</sup><sub>c</sub>(0x03||A<sup>P</sup>||i), i < 2<sup>31</sup>;</p>
<p align="center">Z<sub>i</sub> &larr; F<sup>P</sup><sub>c</sub>(0x01||K<sup>P</sup>||i), i &ge; 2<sup>31</sup>;</p>

<p>Where the output of the HMAC function truncated to the right 32 bytes.</p>


<h4>E. Key tree</h4>

<p>Child with i < 2<sup>31</sup> can be a parent for his children with his own chain code c<sub>i</sub>. Proceeding with this, we can create a tree of keys where each non-leaf node is a parent for its children and is a child for its parent. A path m &rarr; i<sub>1</sub> &rarr; ⋯ &rarr; i<sub>l</sub>  from the original parent m to a child at level l thus uniquely identifies the node.</p>

<p>Eventually, it is evident that Ed25519 is one of the best available Public-key signatures until now which is going to be used for digital signatures. We may change the Public-key signature if we find some flaw in Ed25519 or if we find another Public-key signature algorithm which offers higher assurance and performance. We picked Ed25519 algorithm because of the advantages this algorithm offering. For more in-depth information about Ed25519 features please visit <a href="https://ed25519.cr.yp.to/" target="_blank" rel="external">Ed25519</a> official website.</p>

<p>Eventually, it is evident that Ed25519 is one of the best available Public-key signatures until now which is going to be used for digital signatures. We may change the Public-key signature if we find some flaw in Ed25519 or if we find another Public-key signature algorithm which offers higher assurance and performance. We picked Ed25519 algorithm because of the advantages this algorithm offering. For more in-depth information about Ed25519 features please visit <a href="https://ed25519.cr.yp.to/" target="_blank" rel="external">Ed25519</a> official website.	</p>

</font>
</div>

<div align="justify">
<font face="cambria" >

<h2><a id="Why-Equihash"></a>1.3. Why Equihash?</h2>

<p>There are four main consensus mechanisms, a consensus mechanism is fundamental problem in distributed computing and multi-agent systems is to achieve overall system reliability in the presence of a number of faulty processes. These mechanisms listed as below:</p>

<ul>
	<li>Proof-of-Authority</li>
	<li>Proof-of-Space</li>
	<li>Proof-of-Stake</li>
	<li>Proof-of-Work </li>
<ul>

</font>
</div>

<div align="center">
<font face="cambria" >

 <table>
   <TR>
      <TH COLSPAN="5">List of cryptocurrencies with Proof-of-Work consensus mechanism</TH>
   </TR>
   <TR ALIGN="CENTER">
      <TD><b>SHA-256-based</b></TD>
      <TD><b>Equihash-based</b></TD>
      <TD><b>Ethash-based</b></TD>
      <TD><b>Scrypt-based</b></TD>
      <TD><b>CryptoNote-based</b></TD>
	  </TR>
   <TR ALIGN="CENTER">
      <TD>Bitcoin</TD>
      <TD>Zcash</TD>
      <TD>Ethereum</TD>
      <TD>Dogecoin</TD>
      <TD>Bytecoin</TD>
	  </TR>
   <TR ALIGN="CENTER">
      <TD>Titcoin</TD>
      <TD>Zcoin</TD>
      <TD>Ubiq</TD>
      <TD>PotCoin</TD>
      <TD>Monero</TD>
	  </TR>
   <TR ALIGN="CENTER">
      <TD>Peercoin</TD>
      <TD>Zclassic</TD>
      <TD>KodakCoin</TD>
      <TD>Litecoin</TD>
	  </TR>
   <TR ALIGN="CENTER">
      <TD>NuBits</TD>
      <TD>Bitcoin Gold</TD>
      <TD>Ethereum Classic</TD>
      <TD>Gulden</TD>
	  </TR>
   <TR ALIGN="CENTER">
      <TD>Namecoin</TD>
      <TD>Komodo</TD>
	  </TR>
   <TR ALIGN="CENTER">
      <TD>Factom</TD>
	  </TR>
   <TR ALIGN="CENTER">
      <TD>Bitcoin Cash</TD>
	  </TR>
	  </TABLE>

</div>



<div align="justify">
<font face="cambria" >

<p>In proof-of-work mining, miners are tasked with generating a short binary blob (called a nonce), which, when hashed, produces an output value less than a pre-specified target threshold. Due to the cryptographic nature of each currency’s hash function, there is no way to reverse-engineer or back-compute a nonce that satisfies the target threshold limit. Instead, miners must “guess-and-check” hashes as fast as possible, and hope they’re the first miner in the entire crypto-currency’s network to find a valid nonce.</p>

<p>There are variety of algorithms based on this consensus mechanism such as Equihash and Ethash. Equihash is a memory-oriented Proof-of-Work algorithm developed by the University of Luxembourg's Interdisciplinary Centre for Security, Reliability and Trust (SnT). Zcash, Zcoin, Zclassic, Bitcoin Gold and Komodo all using Equihash while Ethereum, Ethereum Classic, KodakCoin and Ubiq are using Ethash. Equihash is a memory-oriented Proof-of-Work, which means how much mining one can do is mostly determined by how much RAM the computer has. The chart below shows how the Ethash works. The main advantage of Equihash over Ethash is simplicity in algorithm. Equihash having the same speed on both CPU and GPU instead, Ethash has different speeds while running on CPU, GPU and FPGA. Finally, one can calculate the chance of reaching solution/solutions of Equihash by taking advantage of special probability. The diagram of Equihash algorithm is presented below from reference (Biryukov & Khovratovich, 2016):</p>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equihash Algorithm.png"><img align="center" src="images/TrustNote-TR-01-Equihash Algorithm.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >
<p>Finally, we stress that we may change the Proof-of-Work, if we find some defect in Equihash or if we find another Proof-of-Work algorithm which offers higher performance, security and assurance. For more in-depth information about Equihash properties please, see (Biryukov & Khovratovich, 2016).</p>
</font>
</div>

<div align="justify">
<font face="cambria" >

<h1><a id="Introduction-&-Mathematical-foundation"></a>2. Introduction & Mathematical foundation</h1>
<h2><a id="Blake2"></a>2.1. Blake2</h2>

<p>In this section, the parameters and mathematical foundation of Blake2 (Blake2b and Blake2s) will be explained; adopted from reference (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013).</p>
</font>
</div>

<div align="center">
<font face="cambria" >
<p><b>Parameter Blocks of Blake2b and Blake2s</b></p>



<TABLE ALIGN="CENTER">
   <TR>
      <TH>Offset</TH>
      <TH>0</TH>
      <TH>1</TH>
      <TH>2</TH>
      <TH>3</TH>
	  </TR>
   <TR ALIGN="CENTER">
      <TH>0</TH>
      <TH>Digest length</TH>
      <TH>Key length</TH>
      <TH>Fanout</TH>
      <TH>Depth</TH>
   </TR>
   <TR ALIGN="CENTER">
      <TH>4</TH>
      <TH COLSPAN="4">Leaf length</TH>
   </TR>
    <TR ALIGN="CENTER">
      <TH><p>8</p><p>12</p></TH>
      <TH COLSPAN="4">Node offset</TH>
   </TR>
      <TR ALIGN="CENTER">
      <TH>16</TH>
      <TH>Node depth</TH>
      <TH>Inner length</TH>
      <TH COLSPAN="2">RFU</TH>
  </TR>
    <TR ALIGN="CENTER">
      <TH><p>20</p><p>24</p><p>28</p></TH>
      <TH COLSPAN="4">RFU</TH>
   </TR>
    <TR ALIGN="CENTER">
      <TH><p>32</p><p>...</p><p>44</p></TH>
      <TH COLSPAN="4">Salt</TH>
   </TR>
    <TR ALIGN="CENTER">
      <TH><p>48</p><p>...</p><p>60</p></TH>
      <TH COLSPAN="4">Personalization</TH>
   </TR>
   </TABLE>
<p><b>BLAKE2b parameter block structure (offsets in bytes)</b></p>

<TABLE align="center">
   <TR>
      <TH>Offset</TH>
      <TH>0</TH>
      <TH>1</TH>
      <TH>2</TH>
      <TH>3</TH>
	  </TR>
   <TR ALIGN="CENTER">
      <TH>0</TH>
      <TH>Digest length</TH>
      <TH>Key length</TH>
      <TH>Fanout</TH>
      <TH>Depth</TH>
   </TR>
   <TR ALIGN="CENTER">
      <TH>4</TH>
      <TH COLSPAN="4">Leaf length</TH>
   </TR>
   <TR ALIGN="CENTER">
      <TH>8</TH>
      <TH COLSPAN="4">Node offset</TH>
   </TR>
     <TR ALIGN="CENTER">
      <TH>12</TH>
      <TH COLSPAN="2">Node depth</TH>
      <TH>Inner length</TH>
      <TH>RFU</TH>
		</TR>
	<TR ALIGN="CENTER">
      <TH><p>16</p><p>20</p></TH>
      <TH COLSPAN="4">Salt</TH>
    </TR>
	<TR ALIGN="CENTER">
      <TH><p>24</p><p>28</p></TH>
      <TH COLSPAN="4">Personalization</TH>
   </TR>
   </TABLE>

</font>
</div>
<div align="justify">
<font face="cambria" >
<p><b>BLAKE2s parameter block structure (offsets in bytes)</b></p>

<p>General parameters (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>

<ul>
	<li>Digest byte length (1 byte): an integer in [1, 64] for BLAKE2b, in [1, 32] for BLAKE2s</li>
	<li>Key byte length (1 byte): an integer in [0, 64] for BLAKE2b, in [0, 32] for BLAKE2s (set to 0 if no key is used)</li>
	<li>Salt (16 or 8 bytes): an arbitrary string of 16 bytes for BLAKE2b, and 8 bytes for BLAKE2s (set to all-NULL by default)</li>
	<li>Personalization (16 or 8 bytes): an arbitrary string of 16 bytes for BLAKE2b, and 8 bytes for BLAKE2s (set to all-NULL by default)</li>
</ul>

<p>Tree hashing parameters (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>

<ul>
	<li>Fan-out an integer in [0, 255] (set to 0 if unlimited, and to 1 only in sequential mode)</li>
	<li>Maximal depth (1 byte): an integer in [1, 255] (set to 255 if unlimited, and to 1 only in sequential mode)</li>
	<li>Leaf maximal byte length (4 bytes): an integer in [0, 232 - 1], that is, up to 4 GiB (set to 0 if unlimited, or in sequential mode)</li>
	<li>Node offset (8 or 6 bytes): an integer in [0, 264-1] for BLAKE2b, and in [0, 248-1] for BLAKE2s (set to 0 for the first, leftmost, leaf, or in sequential mode)</li>
	<li>Node depth (1 byte): an integer in [0, 255] (set to 0 for the leaves, or in sequential mode)</li>
	<li>Inner hash byte length (1 byte): an integer in [0, 64] for BLAKE2b, and in [0, 32] for BLAKE2s (set to 0 in sequential mode)</li>
</ul>

<h3><a id="Blake2b"></a>2.1.1. Blake2b</h3>

<p>BLAKE2b supports data of any byte length  0 &le; l &le; 2<sup>128</sup> . Data is first padded to form a sequence of N = [l/128] 16-word blocks m<sub>0</sub>,m<sub>1</sub>, ..., m<sub>(N-1)</sub> and then hashed by doing (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>



<p align="center">h<sup>0</sup> &larr; IV &oplus; P</p>
<p align="center">for i = 0 ,… ,N-1</p>
<p align="center">h<sup>(i+1)</sup> &larr; compress(h<sup>i</sup>,m<sup>i</sup>,l<sup>i</sup>)</p>
<p align="center">return h<sup>N</sup></p>



<p>Where l<sup>i</sup> denotes the number of data bytes in m<sup>0</sup>,m<sup>1</sup>, ..., m<sup>(N-1)</sup> (that is, not counting any padding byte), P is the parameter block specified in Parameter Blocks, and IV is (as in BLAKE and SHA-512) the following 64-bit words (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>



<p align="center">IV<sub>0</sub> = 6a09e667f3bcc908&emsp;&emsp;IV<sub>1</sub> = bb67ae8584caa73b</p>
<p align="center">IV<sub>2</sub> = 3c6ef372fe94f82b&emsp;&emsp;IV<sub>3</sub> = a54ff53a5f1d36fa</p>
<p align="center">IV<sub>4</sub> = 510e527fade682d1&emsp;&emsp;IV<sub>5</sub> = 9b05688c2b3e6c1f</p>
<p align="center">IV<sub>6</sub> = 1f83d9abfb41bd6b&emsp;&emsp;IV<sub>7</sub> = 5be0cd19137e2179</p>



<p>The compression function compress takes as input (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>

<ul>
	<li>A 64-byte chain value h = h<sub>0</sub>,...,h<sub>7</sub></li>
	<li>A 128-byte message block m = m<sub>0</sub>,...,m<sub>15</sub></li>
	<li>A counter t = t<sub>0</sub>,t<sub>1</sub>, and finalization flags f<sub>0</sub>,f<sub>1</sub></li>
</ul>

<p>First, compress initializes a 16-word internal state v<sub>0</sub>,...,v<sub>15</sub> that is (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Matrix Blake2.png"><img align="center" width = "650px" height = "100px" src="images/TrustNote-TR-01-Matrix Blake2.png"></a></p>
</div>

<p>Where f<sub>0</sub> and f<sub>1</sub> are the finalization flags. The internal state v is then transformed through a sequence of 12 rounds, where a round does (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>



<p align="center">G<sub>0</sub>(v<sub>0</sub>,v<sub>4</sub>,v<sub>8</sub>,v<sub>12</sub>)&emsp;G<sub>1</sub>(v<sub>1</sub>,v<sub>5</sub>,v<sub>9</sub>,v<sub>13</sub>)&emsp;G<sub>2</sub>(v<sub>2</sub>,v<sub>6</sub>,v<sub>10</sub>,v<sub>14</sub>)&emsp;G<sub>3</sub>(v<sub>3</sub>,v<sub>7</sub>,v<sub>11</sub>,v<sub>15</sub>)</p>
<p align="center">G<sub>4</sub>(v<sub>0</sub>,v<sub>5</sub>,v<sub>10</sub>,v<sub>15</sub>)&emsp;G<sub>5</sub>(v<sub>1</sub>,v<sub>6</sub>,v<sub>11</sub>,v<sub>12</sub>)&emsp;G<sub>6</sub>(v<sub>2</sub>,v<sub>7</sub>,v<sub>8</sub>,v<sub>13</sub>)&emsp;G<sub>7</sub>(v<sub>3</sub>,v<sub>4</sub>,v<sub>9</sub>,v<sub>14</sub>)</p>



<p>That is, a round applies a G function to each of the columns in parallel, and then to all of the diagonals in parallel. The G function of BLAKE2b uses the constants in the table below which is permutations of  f {0,...,15} used by the BLAKE2 functions (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013). </p>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Matrix Blake22.png"><img align="center" width="600px" height="300px" src="images/TrustNote-TR-01-Matrix Blake22.png"></a></p>
</div>

<p>After the 12 rounds, the new chain value h<sup>'</sup><sub>0</sub>,...,h<sup>'</sup><sub>7</sub> is defined as (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013):</p>



<p align="center">h<sup>'</sup><sub>0</sub>=h<sub>0</sub>&oplus;v<sub>0</sub>&oplus;v<sub>8</sub></p>
<p align="center">h<sup>'</sup><sub>1</sub>=h<sub>1</sub>&oplus;v<sub>1</sub>&oplus;v<sub>9</sub></p>
<p align="center">h<sup>'</sup><sub>2</sub>=h<sub>2</sub>&oplus;v<sub>2</sub>&oplus;v<sub>10</sub></p>
<p align="center">h<sup>'</sup><sub>3</sub>=h<sub>3</sub>&oplus;v<sub>3</sub>&oplus;v<sub>11</sub></p>
<p align="center">h<sup>'</sup><sub>4</sub>=h<sub>4</sub>&oplus;v<sub>4</sub>&oplus;v<sub>12</sub></p>
<p align="center">h<sup>'</sup><sub>5</sub>=h<sub>5</sub>&oplus;v<sub>5</sub>&oplus;v<sub>13</sub></p>
<p align="center">h<sup>'</sup><sub>6</sub>=h<sub>6</sub>&oplus;v<sub>6</sub>&oplus;v<sub>14</sub></p>
<p align="center">h<sup>'</sup><sub>7</sub>=h<sub>7</sub>&oplus;v<sub>7</sub>&oplus;v<sub>15</sub></p>



<p>Note the absence of the salt, compared to BLAKE.</p>

<h3><a id="Blake2s"></a>2.1.2. Blake2s</h3>

<p>BLAKE2s supports data of any byte length 0 &le; l &le; 2<sup>64</sup> . It works similarly to BLAKE2b, but on 32-bit words instead of 64-bit words (the byte length of a chaining value, a message block, a counter or finalization flag are thus divided by two). BLAKE2s uses the following IV:</p>



<p align="center">IV<sub>0</sub> = 6a09e667&emsp;&emsp;IV<sub>1</sub> = bb67ae85</p>
<p align="center">IV<sub>2</sub> = 3c6ef372&emsp;&emsp;IV<sub>3</sub> = a54ff53a</p>
<p align="center">IV<sub>4</sub> = 510e527f&emsp;&emsp;IV<sub>5</sub> = 9b05688c</p>
<p align="center">IV<sub>6</sub> = 1f83d9ab&emsp;&emsp;IV<sub>7</sub> = 5be0cd19</p>



<p>BLAKE2s does 10 rounds, and uses the G function. For more in-depth mathematical information about Blake2b and Blake2s, please visit (Aumasson, Neves, Wilcox-O’Hearn, & Winnerlein, 2013).</p>

<h2><a id="Ed25519"></a>2.2. Ed25519</h2>

<p>In this section the mathematical foundation of Ed25519 and the governing algorithm of Ed25519 will be explained. This section adopted from references (Langley, Google, Hamburg, Rambus Cryptography Research, & Turner, 2016), (Josefsson & Liusvaara, 2017). Ed25519:</p>

<ul>
	<li>Uses twisted edwards curve</li>
	<li>Curve used ax<sup>2</sup>+y<sup>2</sup>=1-dx<sup>2</sup>y<sup>2</sup></li>
	<li>Is over the prime field 2<sup>225</sup>-19</li>
	<li>Used for signing and verifying messages</li>
	<li>Published by Daniel Bernstein in 2011</li>
</ul>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Ed25519 Curve.png"><img align="center" src="images/TrustNote-TR-01-Ed25519 Curve.png"></a></p>
</div>

<h3>Ed25519 Terms</h3>

<p><b>A</b> is the public key point</p>
<p><b>a</b> is the public key</p>
<p><b>H(*)</b> is the Blake2 hash of *</p>
<p><b>B</b> is the unique point (x, 4/5) &#8714; E for which x is positive</p>
<p><b>M</b> is the message</p>
<p><b>l</b> is the prime 2<sup>252</sup> + 27742317777372353535851937790883648493</p>

<h3>Ed25519 Sign/Verify</h3>

<p>Steps for signature</p>

<ul>
	<p>1. computing r = H(hb,...,h2b-1,M)</p>
	<p>2. computing R = rB</p>
	<p>3. computing S = (r + H(R,A,M)a) mod l</p>
</ul>

<p>Steps for Verification</p>
<ul>
	<p>1. computing r = H(hb,...,h2b-1,M)</p>
	<p>2. computing R = rB</p>
	<p>3. computing S = (r + H(R,A,M)a) mod l</p>
	<p>4. SB = R + H(R,A,M)A</p>
</ul>

<h4>Ed25519 Signature and Verification Algorithm</h4>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Ed25519 sign.png"><img align="center" height="500px" width="600px" src="images/TrustNote-TR-01-Ed25519 sign.png"></a></p>
<p><a target="_blank" href="images/TrustNote-TR-01-Ed25519 verify.png"><img align="center" height="500px" width="600px" src="images/TrustNote-TR-01-Ed25519 verify.png"></a></p>
</div>

<h4>Ed25519 Fast Single Verify</h4>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Ed25519 fast sign.png"><img align="center" height="500px" width="600px" src="images/TrustNote-TR-01-Ed25519 fast sign.png"></a></p>
</div>

<p>SB = R + H(R,A,M)×A is changed to R = SB - H(R,A,M)A saving having to decompress R</p>

<h3>Parameters</h3>

<ul>

<p>1. An odd prime power p. EdDSA uses an elliptic curve over the finite field GF(p).</p>
<p>2. An integer b with 2(b-1) > p. EdDSA public keys have exactly b bits, and EdDSA signatures have exactly 2b bits. b is recommended to be a multiple of 8, so public key and signature lengths are an integral number of octets.</p>
<p>3. A (b-1)-bit encoding of elements of the finite field GF(p).</p>
<p>4. A cryptographic hash function H producing 2b-bit output. Conservative hash functions (i.e., hash functions where it is infeasible to create collisions) are recommended and do not have much impact on the total cost of EdDSA.</p>
<p>5. An integer c that is 2 or 3. Secret EdDSA scalars are multiples of 2c. The integer c is the base-2 logarithm of the so-called cofactor.</p>
<p>6. An integer n with c &le; n < b. Secret EdDSA scalars have exactly n+1 bits, with the top bit (the 2n position) always set and the bottom c bits always cleared.</p>
<p>7. A non-square element d of GF(p). The usual recommendation is to take it as the value nearest to zero that gives an acceptable curve.</p>
<p>8. A non-zero square element of GF(p). The usual recommendation for best performance is a = -1 if p mod 4 = 1, and a = 1 if p mod 4 = 3.</p>
<p>9. An element B &ne;(0,1) of the set E = { (x,y)&#8714; GF(p)× GF(p) ||  ax<sup>2</sup>+y<sup>2</sup>=1-dx<sup>2</sup>y<sup>2</sup>  } .</p>
<p>10. An odd prime L such that [L]B = 0 and 2x<sup>c</sup> L = #E. The number #E (the number of points on the curve) is part of the standard data provided for an elliptic curve E, or it can be computed as cofactor * order.</p>
<p>11. A "prehash" function PH. PureEdDSA means EdDSA where PH is the identity function, i.e.,PH(M)= M. HashEdDSA means EdDSA where PH generates a short output, no matter how long the message is; for example, PH(M)= Hash(M).</p>
<p>12. Points on the curve form a group under addition, (x<sub>3</sub>,y<sub>3</sub>)  = (x<sub>1</sub>,y<sub>1</sub>)  + (x<sub>2</sub>,y<sub>2</sub>), with the formulas:</p>

</ul>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equation Ed25519.png"><img align="center" src="images/TrustNote-TR-01-Equation Ed25519.png"></a></p>
</div>

<p>The neutral element in the group is (0,1). Unlike many other curves used for cryptographic applications, these formulas are "complete"; they are valid for all points on the curve, with no exceptions. In particular, the denominators are non-zero for all input points. There are more efficient formulas, which are still complete, that use homogeneous coordinates to avoid the expensive modulo p inversions. Ed25519 is EdDSA instantiated with:</p>

<p><b>p</b> 2<sup>255</sup> - 19</p>
<p><b>b</b> 256</p>
<p><b>Encoding of GF(p)</b> 255-bit little-endian encoding of {0,1,...,p-1}</p>
<p><b>c</b> log<sub>2</sub>⁡(cofactor of edwards25519)</p>
<p>Cofactor of edwards25519 = 8</p>
<p><b>n</b> 254</p>
<p><b>d</b> 37095705934669439343138083508754565189542113879843219016388785533085940283555</p>
<p><b>a</b> -1</p>
<p><b>B(X(P),Y(P))</b> of edwards25519</p>
<p><b>X(P)</b> 15112221349535400772501151409588531511454012693041857206046113283949847762202</p>
<p><b>Y(P)</b> 46316835694926478169428394003475163141307993866256225615783033603165251855960</p>
<p><b>L</b> order 2<sup>252</sup>  + 0x14def9dea2f79cd65812631a5cf5d3ed</p>

<h3>Modular Arithmetic</h3>

<p>For advice on how to implement arithmetic modulo p = 2<sup>255</sup> - 19 efficiently and securely, see Curve25519 (Josefsson & Liusvaara, 2017). For inversion modulo p, it is recommended to use the identity x<sup>(-1)</sup>  = x<sup>(p-2)</sup> (mod p). Inverting zero should never happen, as it would require invalid input, which would have been detected before, or would be a calculation error. For point decoding or "decompression", square roots modulo p are needed. They can be computed using the Tonelli-Shanks algorithm or the special case for p = 5 (mod 8). To find a square root of a, first compute the candidate root x = a<sup>(p+3)/8</sup> (mod p). Then there are three cases:</p>

<ul>
	<p>1. x<sup>2</sup>  = a (mod p). Then x is a square root.</p>
	<p>2. x<sup>2</sup> = -a (mod p). Then 2<sup>(p-1)/4</sup> x is a square root.</p>
	<p>3. a is not a square modulo p.</p>
</ul>

<h3>Encoding</h3>

<p>All values are coded as octet strings, and integers are coded using little-endian convention, i.e., a 32-octet string h = h[0],...,h[31] represents the integerh[0] + 2<sup>8</sup>  * h[1] + ...+ 2<sup>248</sup>  * h[31]. A curve point (x,y), with coordinates in the range 0 &le; x,y < p, is coded as follows. First, encode the y-coordinate as a little-endian string of 32 octets. The most significant bit of the final octet is always zero. To form the encoding of the point, copy the least significant bit of the x-coordinate to the most significant bit of the final octet.</p>

<h3>Decoding</h3>

<p>Decoding a point, given as a 32-octet string, is a little more complicated.</p>

<ul>
	<p>1. First, interpret the string as an integer in little-endian representation. Bit 255 of this number is the least significant bit of the x-coordinate and denote this value x<sub>0</sub> . The y-coordinate is recovered simply by clearing this bit. If the resulting value is &ge; p, decoding fails.</p>
	<p>2. To recover the x-coordinate, the curve equation implies x<sup>2</sup> = (y<sup>2</sup>-1)/(dy<sup>2</sup>+1) (mod p). The denominator is always non-zero mod p. Let u = y<sup>2</sup> - 1 and v = dy<sup>2</sup> + 1. To compute the square root of (u/v), the first step is to compute the candidate root x = (u/v)<sup>(p+3)/8</sup>. This can be done with the following trick, using a single modular powering for both the inversion of v and the square root:</p>

</ul>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equation1 Ed25519.png"><img align="center" src="images/TrustNote-TR-01-Equation1 Ed25519.png"></a></p>
</div>

<ul>
	<p>3. Again, there are three cases:</p>
	<ul>
		<p>3.1. If vx<sup>2</sup>  = u (mod p), x is a square root.</p>
		<p>3.2. If vx<sup>2</sup>  = -u (mod p), set x &larr; x2<sup>(p-1)/4</sup>, which is a square root.</p>
		<p>3.3. Otherwise, no square root exists for modulo p, and decoding fails.</p>
	</ul>
	<p>4. Finally, use the x<sub>0</sub> bit to select the right square root. If x = 0, and x<sub>0</sub>  = 1, decoding fails. Otherwise, if x<sub>0</sub> &ne; x mod 2, set x &larr; p - x. Return the decoded point (x,y).</p>
</ul>

<h3>Point Addition</h3>

<p>For point addition, the following method is recommended. A point (x,y) is represented in extended homogeneous coordinates (X,Y,Z,T), with x = X/Z, y = Y/Z, xy = T/Z. The neutral point is (0,1), or equivalently in extended homogeneous coordinates (0,Z,Z,0) for any non-zero Z. The following formulas for adding two points, (x<sub>3</sub>,y<sub>3</sub>)=(x<sub>1</sub>,y<sub>1</sub>)+(x<sub>2</sub>,y<sub>2</sub>), on twisted Edwards curves with a = -1, square a, and non-square d are described in Section 3.1 of <a href="http://eprint.iacr.org/2008/" target="_blank" rel="external">Edwards-revisited</a> and in <a href="http://www.hyperelliptic.org/EFD/g1p/auto-twisted-extended-1.html#addition-add-2008-hwcd-3)." target="_blank" rel="external">EFD-TWISTED-ADD</a>. They are complete, i.e., they work for any pair of valid input points. </p>



<p align="center">A = (Y<sub>1</sub> - X<sub>1</sub>)(Y<sub>2</sub> - X<sub>2</sub>)</p>
<p align="center">B = (Y<sub>1</sub> + X<sub>1</sub>)(Y<sub>2</sub> + <sub>2</sub>)</p>
<p align="center">C = T<sub>1</sub>2dT<sub>2</sub></p>
<p align="center">D = Z<sub>1</sub>2Z<sub>2</sub></p>
<p align="center">E = B - A</p>
<p align="center">F = D - C</p>
<p align="center">G = D + C</p>
<p align="center">H = B + A</p>
<p align="center">X<sub>3</sub> = E * F</p>
<p align="center">Y<sub>3</sub> = G * H</p>
<p align="center">T<sub>3</sub> = E * H</p>
<p align="center">Z<sub>3</sub> = F * G</p>



<p>For point doubling, (𝑥<sub>3</sub>,𝑦<sub>3</sub>) = (𝑥<sub>1</sub>,𝑦<sub>1</sub>) + (𝑥<sub>1</sub>,𝑦<sub>1</sub>), one could just substitute equal points in the above (because of completeness, such substitution is valid) and observe that four multiplications turn into squares. However, using the formulas described in Section 3.2 of <a href="http://eprint.iacr.org/2008/" target="_blank" rel="external">Edwards-revisited</a> and in <a href="http://www.hyperelliptic.org/EFD/g1p/auto-twisted-extended-1.html#addition-add-2008-hwcd-3)." target="_blank" rel="external">EFD-TWISTED-ADD</a> saves a few smaller operations.</p>



<p align="center">A = X<sup>2</sup><sub>1</sub></p>
<p align="center">B = Y<sup>2</sup><sub>1</sub></p>
<p align="center">C = 2Z<sup>2</sup><sub>1</sub></p>
<p align="center">H = A + B</p>
<p align="center">E = H -(X<sub>1</sub> + Y<sub>1</sub>)<sup>2</sup></p>
<p align="center">G = A - B</p>
<p align="center">F = C + G</p>
<p align="center">X<sub>3</sub> = E * F</p>
<p align="center">Y<sub>3</sub> = G * H</p>
<p align="center">T<sub>3</sub> = E * H</p>
<p align="center">Z<sub>3</sub> = F * G</p>




<h3>Key Generation</h3>

<p>The private key is 32 octets (256 bits, corresponding to b) of cryptographically secure random data. See RFC4086 for a discussion about randomness. The 32-byte public key is generated by the following steps.</p>

<ul>
	<p>1. Hash the 32-byte private key, storing the digest in a 64-octet large buffer, denoted h. Only the lower 32 bytes are used for generating the public key.</p>
	<p>2. Run the buffer: The lowest three bits of the first octet are cleared, s the highest bit of the last octet is cleared, and the second highest bit of the last octet is set.<p/>
	<p>3. Interpret the buffer as the little-endian integer, forming a secret scalar s. Perform a fixed-base scalar multiplication [s]B.<p/>
	<p>4. 	The public key A is the encoding of the point [s]B. First, encode the y-coordinate (in the range 0 &le; y < p) as a little- endian string of 32 octets. The most significant bit of the final octet is always zero. To form the encoding of the point [s]B, copy the least significant bit of the x coordinate to the most significant bit of the final octet. The result is the public key.<p/>
</ul>

<h3>Sign</h3>

<p>The input to the signing procedure is the private key, a 32-octet string, and a message M of arbitrary size. </p>

<ul>
	<p>1. Hash the private key, 32 octets. Let h denote the resulting digest. Construct the secret scalar s from the first half of the digest, and the corresponding public key A, as described in the previous section. Let prefix denote the second half of the hash digest,h[32],...,h[63].</p>
	<p>2. Compute Hash(M), where M is the message to be signed. Interpret the 64-octet digest as a little- endian integer r.</p>
	<p>3. Compute the point [r]B. For efficiency, do this by first reducing r modulo L, the group order of B. Let the string R be the encoding of this point.</p>
	<p>4. Compute Hash( R || A), and interpret the 64-octet digest as a little-endian integer k.</p>
	<p>5. Compute S = (r + k×s) mod L. For efficiency, again reduce k modulo L first.</p>
	<p>6. Form the signature of the concatenation of R (32 octets) and the little-endian encoding of S (32 octets; the three most significant bits of the final octet are always zero).</p>
</ul>

<h3>Verify</h3>

<ul>
	<p>1. To verify a signature on a message M using public key A, with F being 0 for Ed25519 and if Ed25519 is being used, C being the context, first split the signature into two 32-octet halves. Decode the first half as a point R, and the second half as an integer S, in the range 0 &le; s < L. Decode the public key A as point A<sup>'</sup>. If any of the decodings fail (including S being out of range), the signature is invalid.</p>
	<p>2. Compute Hash(R || A), and interpret the 64-octet digest as a little-endian integer k.</p>
	<p>3. Check the group equation [8][S]B = [8]R + [8][k] A<sup>'</sup>. It's sufficient, but not required, to instead check [S]B = R + [k] A<sup>'</sup>.</p>
</ul>

<h2><a id="Equihash"></a>2.3. Equihash</h2>

<p>Wagner exposes the generalized birthday problem and the algorithm for it (Wagner, 2002). The generalized birthday problem for one list is formulated as follows: given list L of n-bit strings {X<sub>i</sub>}, find distinct {X<sub>i<sub>j</sub></sub>} such that (Biryukov & Khovratovich, 2016):</p>

<p align="center">X<sub>i<sub>1</sub></sub> &oplus; X<sub>i<sub>2</sub></sub> &oplus; ... &oplus; X<sub>i<sub>3</sub></sub> = 0</p>

<p>Wagner considers the setting where {X<sub>i</sub>} are outputs of some (non-keyed) PRNG, e.g. a hash function H in the counter mode. Thus Wagner had to find {i<sub>j</sub>} such that (Biryukov & Khovratovich, 2016):</p>

<p>H(i<sub>1</sub>) &oplus; H(i<sub>2</sub>) &oplus; ... &oplus; H(i<sub>3</sub>)=0</p>


<p>For k = 1 this problem is the collision search, and can be solved trivially by sorting in 2<sup>(n/2)</sup> time and space complexity if |L| > 2<sup>(n/2)</sup>. However, for k > 1 and smaller lists the problem is harder. For instance, from the information-theoretic point of view a solution for k = 2 in a list of size 2<sup>(n/4)</sup> is expected, but no algorithm faster than 2<sup>(n/3)</sup> operations is known (Biryukov & Khovratovich, 2016).</p>

<p>Wagner demonstrated an algorithm for k > 1 and the lists are large enough to contain numerous solutions. It has time and space complexity of O(2<sup>n/(k+1)</sup>) for lists of the same size. Wagner’s algorithm generalizes easily to some operations other than XOR (e.g., to the modular addition). Also note that for k log_2⁡n a XOR solution can be found by the much faster Gaussian elimination with complexity of O(2<sup>k</sup>) string operations. The table below adopted from (Wagner, 2002) with some modifications explains the basic Wagner algorithm for the generalized birthday problem.</p>



 <table>
   <TR>
      <TH><b>Basic Wagner’s algorithm for the generalized birthday problem</b></TH>
   </TR>
    <TR>
      <TD>
	  <p align="justify"><b>Input:</b> list L of N n-bit strings (N&Lt;2<sup>n</sup>).</p>
  <ul>

<p align="justify">(1) Enumerate the list as {X<sub>1</sub>,…,X<sub>N</sub>} and store pairs (X<sub>j</sub>,j) in a table.</p>
<p align="justify">(2) Sort the table by X<sub>j</sub>. Then find all unordered pairs (i,j) such that X<sub>i</sub> collides with X<sub>j</sub> on the first n/(k+1) bits. Store all tuples (X<sub>(i,j)</sub>=X<sub>i</sub> &oplus; X<sub>j</sub>,i,j) in the table.</p>
<p align="justify">(3) Repeat the previous step to find collisions in X<sub>(i,j)</sub> on the next n/(k+1) bits and store the resulting tuples (X<sub>(i,j,k,l)</sub>,i,j,k,l) in the table.</p>
<p align="justify">(4) […] Repeat the previous step for the next n/(k+1) bits, and so on until only 2n/(k+1) bits are non-zero.</p>
<p align="justify">(5) [k+1] At the last step, find a collision on the last 2n/(k+1) bits. This gives a solution to the original problem.</p>

  </ul>

  <p align="justify"><b>Output:</b> list {i<sub>j</sub>} conforming to H(i<sub>1</sub>) &oplus; H(i<sub>2</sub>) &oplus; ... &oplus; H(i<sub>3</sub>)=0.</p>
  </TD>
   </TR>
 <table>


</font>
</div>

<div align="justify">
<font face="cambria" >

<p>Assume that sorting l = O(N) elements is computationally equivalent to l calls to the hash function H. Let a single call to H be the time unit (Biryukov & Khovratovich, 2016).</p>

<p><b>Proposition 1.</b> For N = 2<sup>(n/(k+1))</sup>+1 and k<sup>2</sup> < n Algorithm above produces two solutions (on average) using (2<sup>(k-1)</sup>+n)N/8   bytes of memory in time (k+1)N (Biryukov & Khovratovich, 2016).</p>

<p><b>Proof.</b> Suppose N = 2<sup>(n/(k+1))</sup>+1 tuples stored at the first step. Then after collision search it is expected to have: (Biryukov & Khovratovich, 2016):</p>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equation Equihash.png"><img align="center" width="160px" height="80px" src="images/TrustNote-TR-01-Equation Equihash.png"></a></p>
</div>

<p>Entries for the second table, then N - 3 entries for the third table, and so on. Before the last (k-th) collision search it is expected to N - 2<sup>(k-1)</sup> + 1 is approximatly N = 2<sup>(n/(k+1))</sup> + 1 entries, thus on average two solutions after the last step were obtained. The computational complexity is dominated by the complexity of list generation (N hash calls) and subsequent k sorting of N elements. Therefore, the total computational complexity is equivalent to (Biryukov & Khovratovich, 2016):</p>



<p align="center">(k + 1)N = (k + 1)N = 2<sup>(n/(k+1))</sup> + 1</p>



<p>Hash function calls. This ends the proof. Biryukov et. al have not computed the variance of the number of solutions, but their experiments demonstrate that the actual number of solutions at each step is very close (within 10%) to the expected number. If larger lists are used, the table will grow in size over the steps. The list size is exactly taken so that the expected number of solutions is small and the table size does not change much (Biryukov & Khovratovich, 2016).</p>

<p>The generalized birthday problem in its basic form lacks some necessary properties as a proof-of-work. The reason is that Wagner’s algorithm can be iterated to produce multiple solutions by selecting other sets of colliding bits or using more sophisticated techniques. If more memory is available, these solutions can be produced at much lower amortized cost (Proposition 3). Since this property violates the non-amortization requirement for the PoW (see [6]), it was suggested to modify the problem so that only two solutions can be produced on average (Biryukov & Khovratovich, 2016).</p>

<p>This modification is inspired by the fact that a solution found by Wagner’s algorithm carries its footprint. Namely, the intermediate 2<sup>l</sup>-XORs have leading nl/(k+1) bits, for example X<sub>i<sub>4</sub></sub> &oplus; X<sub>i<sub>5</sub></sub> &oplus; X<sub>i<sub>6</sub></sub> &oplus; X<sub>i<sub>7</sub></sub> collide on certain 2n/(k+1) bits. Therefore, if the positions are pre-fixed, where 2<sup>l</sup>-XORs have zero bits, the user will be bind to a particular algorithm flow. Moreover, it has been proven that the total number of possible solutions that conform to these restrictions is only 2 on average, so that the problem becomes amortization-free for given input list L. Only duplicate solutions should be taken care of which appear by swapping 2<sup>l</sup>-XORs within the 2<sup>l</sup>-XORs, for any l. It is simply required that every 2<sup>l</sup>-XORs is ordered as a pair, e.g. with lexicographic order. It should be considered that a certain order is a prerequisite as otherwise duplicate solutions (produced by swaps in pairs, swaps of pairs, etc.) would be accepted. With this modification the Gaussian elimination algorithm does not apply any longer, so larger k can be adopted with no apparent drop in complexity (Biryukov & Khovratovich, 2016).</p>

<p><b>Proposition 2.</b> Optimized Wagner’s algorithm below which adopted from (Biryukov & Khovratovich, 2016) with some changes:</p>



 <table>
   <TR>
      <TH><b>Optimized Wagner’s algorithm for the generalized birthday problem</b></TH>
   </TR>
    <TR>
      <TD>
	  <p align="justify"><b>Input:</b> list L of N n-bit strings.</p>
 <ul>
<p align="justify">(1) Enumerate the list as {X<sub>1</sub>,…,X<sub>N</sub>} and store pairs (j) in a table.</p>
<p align="justify">(2) Sort the table by X<sub>j</sub>, computing it on-the-fly. Then find all unordered pairs (i,j) such that X<sub>i</sub> collides with X<sub>j</sub> on the first n/(k+1) bits. Store all such pairs (i,j) in the table.</p>
<p align="justify">(3) Repeat the previous step to find collisions in X<sub>(i,j)</sub> (again recomputing on-the-fly) on the next n/(k+1) bits and store the resulting tuples (i,j,k,l) in the table.</p>
<p align="justify">(4) […] Repeat the previous step for the next n/(k+1) bits, and so on. When indices trimmed to 8 bits plus the length X<sub>(i,j,…)</sub> becomes smaller than the full index tuple, switch to trimming indices.</p>
<p align="justify">(5) [k+1] At the last step, find a collision on the last 2n/(k+1) bits. This gives a solution to the original problem.</p>

  </ul>

  <p align="justify"><b>Output:</b> list {i<sub>j</sub>} conforming to H(i<sub>1</sub>) &oplus; H(i<sub>2<sup>k</sup></sub>) &oplus; ... &oplus; H(i<sub>3</sub>)=0.</p>
	  </TD>
   </TR>
 <table>

</font>
</div>

<div align="justify">
<font face="cambria" >

<p>For N = 2<sup>(n/(k+1))</sup>+1 runs in M(n,k) = 2<sup>(n/(k+1))</sup>(2<sup>2</sup>+(n/2(k+1))) bytes of memory and T(n,k) = k2<sup>((n/(k+1))+2)</sup> time (Biryukov & Khovratovich, 2016).</p>

<p><b>Proposition 3.</b> Using qM(n,k) memory, a user can find 2q<sup>(k+1)</sup> solutions with costqT(n,k), so that the amortized cost drops by q<sup>(k+1)</sup> (Biryukov & Khovratovich, 2016).</p>

<p><b>Proposition 4.</b> Using M(n,k) = q memory, a user can find 2 solutions in timeC1(q)T(n,k), where [6]:</p>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equation1 Equihash.png"><img align="center"  src="images/TrustNote-TR-01-Equation1 Equihash.png"></a></p>
</div>

<p>Therefore, Wagner’s algorithm for finding 2<sup>k</sup>-XOR has a tradeoff of steepness  (k-1)/2. At the cost of increasing the solution length, the penalty for memory-reducing users can increase (Biryukov & Khovratovich, 2016).</p>

<p><b>Proposition 5.</b> Using constant memory, a user can find one algorithm-bound solution in time (Biryukov & Khovratovich, 2016).</p>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equation4 Equihash.png"><img align="center" src="images/TrustNote-TR-01-Equation4 Equihash.png"></a></p>
</div>

<p><b>Proposition 6.</b> Using M(n,k)/q memory, a user can find 2 algorithm-bound solutions in time C<sub>2</sub> (q)T(n,k), where (Biryukov & Khovratovich, 2016):</p>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equation3 Equihash.png"><img align="center" src="images/TrustNote-TR-01-Equation3 Equihash.png"></a></p>
</div>

<p>Therefore, the algorithm-bound proof-of-work has higher steepness (k/2), and the constant is larger. Thus far it have been equalized the time and computational complexity, whereas an ASIC-equipped user or one with a multi-core cluster would be motivated to parallelize the computation if this reduces the AT cost [ (Biryukov & Khovratovich, 2016).</p>

<p><b>Proposition 7.</b> With p &Lt; T(n,k) processors and M(n,k) shared memory a user can find 2 algorithm-bound solutions in time.</p>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Equation2 Equihash.png"><img align="center" src="images/TrustNote-TR-01-Equation2 Equihash.png"></a></p>
</div>

<p>Additionally, the memory bandwidth grows by the factor of p. For fixed memory size, memory chips with bandwidth significantly higher than that of typical desktop memory (such as DDR3) are rare. Assuming that a prover does not have access to memory with bandwidth higher than certain Bwmax (maximum bandwidth), one can efficiently bound the time-memory (and thus the time-area) product for such implementations (Biryukov & Khovratovich, 2016).</p>

<p>To generate an instance for the proof protocol, a verifier selects a cryptographic hash function H and integers n,k,d which determine time and memory requirements as follows (Biryukov & Khovratovich, 2016):</p>

<ul>
	<li>Memory M is 2<sup>(n/(k+1))</sup>+k</li>
	<li>Time T is (k+1) 2<sup>((n/(k+1))+ d)</sup>  calls to the hash function H.</li>
	<li>Solution size is 2<sup>k</sup>((n/(k+1)) + 1) + 160 bits.</li>
	<li>Verification cost is 2<sup>k</sup> hashes and XORs.</li>

</ul>

<p>Then by selecting a seed I (which may be a hash of transactions, block chaining variable, etc.) and the prover will be tasked with finding 160-bit nonce V and ((n/k+1)+1)-bit x<sub>1</sub>,x<sub>2</sub>,...,x<sub>2<sup>k</sup></sub> such that (Biryukov & Khovratovich, 2016):</p>

<h4>Generalized Birthday - Condition</h4>

<p align="center">H(I||V||x<sub>1</sub>) &oplus; H(I||V||x<sub>2</sub>) &oplus; ... &oplus; H(I||V|| x<sub>2<sup>k</sup></sub>) = 0</p>

<h4>Difficulty - Condition</h4>

<p align="center">H(I||V|| x<sub>1</sub> || x<sub>2</sub> || ... || x<sub>2<sup>k</sup></sub> ) has d leading zeroes</p>

<h4>Algorithm Binding - Condition</h4>

<p align="center">H(I||V|| x<sub>w2<sup>l</sup>+1</sub> ) &oplus; ... &oplus; H(I||V||x<sub>w2<sup>l</sup>+2<sup>l-1</sup></sub>) has  nl/(k+1)  leading zeroes for all w,l  </p>

<p align="center">(x<sub>(w2<sup>l</sup>+1</sub> ||x<sub>w2<sup>l</sup>+2</sub> ||...||x<sub>w2<sup>l</sup>+2<sup>l-1</sup></sub>)<(x<sub>w2<sup>l</sup>+2<sup>l-1</sup>+1</sub> ||x<sub>w2<sup>l</sup>+2<sup>l-1</sup>+2</sub> ||...||x<sub>w2<sup>l</sup>+2<sup>l</sup></sub>) lexicographically</p>

<p align="center">For all l &#8714; {1,…,k-1}  and For all w&#8714;{0, …, 2<sup>k-l</sup> - 1}</p>

<p>Here the order is lexicographical. A prover is supposed to run Wagner’s algorithm and then H. For more information about the Equihash and proof of propositions please, see reference (Biryukov & Khovratovich, 2016).</p>

</font>
</div>

<div align="justify">
<font face="cambria" >

<h1><a id="How-to-get-started-with-it"></a>3. How to get started with it?</h1>

<p>In this section the packages related to each algorithm, parameters required to use them and the test results will be presented. Each subsection introducing the test vectors or testing parameters.</p>

<h2><a id="Lets-get-started-with-Blake2-Node-js-Addon"></a>3.1. Let's get started with Blake2-Node.js-Addon</h2>

<p>In this section the performance of two sets of packages created for Blake2 will be compared. These packages which are forked from other projects; one is the Pure JavaScript implementation of Blake2 and the other one is Node.js C/C++ Addon created for Blake2. The difference is crystal clear in the name, but the main differences are going to be shown in the subsections below. This package is in accordance with Blake2 RCF 7693 Standard, the final results also compared as well; more test vectors can be accessed there as well.</p>

</font>
</div>

<div align="justify">
<font face="cambria" >

<h3><a id="Blake2-Pure-JavaScript-Node-Addon"></a>3.1.1. Blake2 Pure JavaScript-Node-Addon</h3>

<p>This packages which is forked and created from other projects, is tested for generating hash using Blake2b and Blake2s. A JavaScript code is created to test the performance of the package which is available at Appendix A: Blake2b-PureJava-test. The result of hashing “abc” as the input string presented below:</p>

<p>ba80a53f981c4d0d6a2797b69f12f6e94c212f14685ac4b74b12bb6fdbffa2d17d87c5392aab792dc252d5de4533cc9518d38aa8dbf1925ab92386edd4009923</p>

<p>The picture below is the test result of “<b>abc</b>” published in <a href="https://tools.ietf.org/html/rfc7693" target="_blank" rel="external">RCF 7693</a>:</p>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Blake2b-512.png"><img align="center" src="images/TrustNote-TR-01-Blake2b-512.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >

<p>The result of calculating the number of hashes Blake2b - Pure JavaScript can generate: <b>219,743</b> Blake2b with the digest length of 512 bits in 5 second.</p>

<p>Performing the same test for the Blake2s, with the input vector of “<b>abc</b>” and by developing a JavaScript code available at Appendix B: Blake2s-PureJava-test.</p>

<p>508c5e8c327c14e2e1a72ba34eeb452f37458b209ed63a294d999b4c86675982</p>

<p>The picture below is the test result of “<b>abc</b>” published in <a href="https://tools.ietf.org/html/rfc7693" target="_blank" rel="external">RCF 7693</a>:</p>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Blake2s-256.png"><img align="center" src="images/TrustNote-TR-01-Blake2s-256.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >

<p>The result of calculating the number of hashes Blake2s - Pure JavaScript can generate: <b>450,680</b> Blake2s with the digest length of 256 bits in 5 second.</p>

</font>
</div>

<div align="justify">
<font face="cambria" >

<h3><a id="Blake2-C-Node-Addon"></a>3.1.2. Blake2 C/C++ Node-Addon</h3>

<p>This package is forked from other projects and developed to create a C/C++ Node.js Addon. The difference is JavaScript packages are slower as JavaScript is a high level programming language. The main platform in TrustNote is Node.js; therefor to have the best performance while using the basis platform, it will be required to create a C/C++ Addon. Consequently, a JavaScript code will be used as the interface and the calculation will be done in C/C++ core which this favors the performance. The performance of the same functions with the same input in this package will be presented.</p>

<p>Same as previous section the test is to create hash using Blake2b and Blake2s with the digest length of 512 and 256 respectively. A JavaScript code is created to test the performance of the package which is available at Appendix C: Blake2b-C/C++ Node.js-Addon-test.</p>

<p>The result of hashing “<b>abc</b>” as the input string presented below:</p>

<p>ba80a53f981c4d0d6a2797b69f12f6e94c212f14685ac4b74b12bb6fdbffa2d17d87c5392aab792dc252d5de4533cc9518d38aa8dbf1925ab92386edd4009923</p>

<p>The picture below is the test result of “<b>abc</b>” published in <a href="https://tools.ietf.org/html/rfc7693" target="_blank" rel="external">RCF 7693</a>:</p>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Blake2b-512.png"><img align="center" src="images/TrustNote-TR-01-Blake2b-512.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >

<p>The result of calculating the number of hashes Blake2b - Pure JavaScript can generate: <b>6,605,304</b> Blake2b with the digest length of 512 bits in 5 second.</p>

<p>Performing the same test for the Blake2s, with the input vector of “abc” and by developing a JavaScript code available at Appendix D: Blake2s-C/C++ Node.js-Addon-test. </p>

<p>508c5e8c327c14e2e1a72ba34eeb452f37458b209ed63a294d999b4c86675982</p>

</font>
</div>

<div align="center">
<p><a target="_blank" href="images/TrustNote-TR-01-Blake2s-256.png"><img align="center" src="images/TrustNote-TR-01-Blake2s-256.png"></a></p>
</div>

<div align="justify">
<font face="cambria" >

<p>The result of calculating the number of hashes Blake2s - Pure JavaScript can generate: <b>7,128,410</b> Blake2s with the digest length of 256 bits in 5 second.</p>

<p>Therefore, it is crystal clear that C/C++ Addon generates <b>6,605,304</b> hashes for Blake2b and <b>7,128,410</b> hashes for Blake2s with maximum digest length while Pure JavaScript generates only <b>219,743</b> hashes for Blake2b and <b>450,680</b> hashes for Blake2s.</p>

</font>
</div>

<div align="justify">
<font face="cambria" >

<h2><a id="Lets-get-started-with-Ed25519-Node-Addon"></a>3.2. Let's get started with Ed25519-Node-Addon</h2>

<p>The previous chapter showed that it's a waste of time to use Pure JavaScript packages for the project. Therefore, only the C/C++ Addon performance tested and presented for this package. The JavaScript code developed to test this package which is forked from other projects, is available at Appendix E: Ed25519-C/C++ Node.js-Addon-test. During 5 seconds, this package generates, signs and verifies 4,198 keys. This package presents an amazing performance.</p>

</font>
</div>

<div align="justify">
<font face="cambria" >

<h2><a id="Lets-get-started-with-Equihash"></a>3.3. Let's get started with Equihash</h2>

<p>This package is forked from other projects. This package will be performed in C/C++ platform. This package tested with different input and, the outcomes are presented in the table below:</p>

</font>
</div>

<div>
<font face="cambria" >

 <table  >
   <TR>
      <TH><b>N (bits)</b></TH>
      <TH><b>K</b></TH>
      <TH><b>Seed</b></TH>
      <TH><b>Time (ms)</b></TH>
      <TH><b>Difficulty</b></TH>
      <TH><b>Solution Size (KB)</b></TH>
      <TH><b>Number of solutions found</b></TH>
	  </TR>
   <TR>
      <TD>100</TD>
      <TD>4</TD>
      <TD>5</TD>
      <TD>5,155</TD>
      <TD>1</TD>
      <TD>81,920</TD>
      <TD>16</TD>
	</TR>
   <TR>
      <TD>100</TD>
      <TD>4</TD>
      <TD>20</TD>
      <TD>15,281</TD>
      <TD>1</TD>
      <TD>81,920</TD>
      <TD>16</TD>
	</TR>
   <TR>
      <TD>108</TD>
      <TD>5</TD>
      <TD>5</TD>
      <TD>2,843</TD>
      <TD>1</TD>
      <TD>25,600 </TD>
      <TD>32</TD>
	</TR>
   <TR>
      <TD>108</TD>
      <TD>5</TD>
      <TD>20</TD>
      <TD>8,499</TD>
      <TD>1</TD>
      <TD>25,600</TD>
      <TD>32</TD>
	</TR>
   <TR>
      <TD>110</TD>
      <TD>4</TD>
      <TD>20</TD>
      <TD>21,967</TD>
      <TD>1</TD>
      <TD>327,680</TD>
      <TD>16</TD>
	</TR>
   <TR>
      <TD>110</TD>
      <TD>4</TD>
      <TD>5</TD>
      <TD>22,062</TD>
      <TD>1</TD>
      <TD>327,680</TD>
      <TD>16</TD>
	</TR>
      <TD>126</TD>
      <TD>5</TD>
      <TD>5</TD>
      <TD>49,077</TD>
      <TD>1</TD>
      <TD>204,800</TD>
      <TD>32</TD>
	</TR>
      <TD>126</TD>
      <TD>5</TD>
      <TD>20</TD>
      <TD>36,797</TD>
      <TD>1</TD>
      <TD>204,800</TD>
      <TD>32</TD>
	</TR>
</table>

</font>
</div>

<div align="justify">
<font face="cambria" >

<h1><a id="Discussion"></a>4. Discussion</h1>

<p>This document aimed to introduce the most important subjects which directly effecting the security and performance of the final product. Eventually, TrustNote will be manipulating Blake2 as its hash function, Ed25519 as its public key generator for signing contracts and Equihash for verification. As mentioned before, this is a work-in-progress so if we find any newer and better algorithm which guarantees security of the users while offering a higher performance, we will replace it with our current packages.</p>

<h1><a id="References"></a>5. References</h1>

<ul>
<p>1. Aumasson , J.-P., Neves , S., Wilcox-O'Hearn, Z., & Winnerlein , C. (2017, 02 22). BLAKE2 — fast secure hashing. Retrieved from BLAKE2: https://Blake2.net/https://Blake2.net/</p>
<p>2. Aumasson, J.-P., Neves, S., Wilcox-O’Hearn, Z., & Winnerlein, C. (2013). BLAKE2: simpler, smaller, fast as MD5.</p>
<p>3. Bernstein, D., Duif, N., Lange, T., Schwabe, P., & Yang, B.-Y. (2011). Ed25519: high-speed high-security signatures.</p>
<p>4. Biryukov, A., & Khovratovich, D. (2016). Equihash: asymmetric proof-of-work based on the Generalized Birthday problem. LEDGER.</p>
<p>5. Chang, S.-j., Perlner, R., Burr, W., Turan, M., Kelsey, J., Paul, S., & Bassham, L. (2012). Third-Round Report of the SHA-3 Cryptographic Hash Algorithm Competition. National Institute for Standards and Technology.</p>
<p>6. Josefsson, S., & Liusvaara, I. (2017). Edwards-Curve Digital Signature Algorithm (EdDSA). Internet Research Task Force.</p>
<p>7. Langley, A., Google, Hamburg, M., Rambus Cryptography Research, & Turner, S. (2016). Edwards-Curve Digital Signature Algorithm.</p>
<p>8. Wagner, D. (2002). A Generalized Birthday Problem. Lecture Notes in Computer Science 2442, 288–303.</p>
</ul>

</font>
</div>
</html>
