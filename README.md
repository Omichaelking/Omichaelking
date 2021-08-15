 !function(e,t){"object"==typeof
exports&&"object"==typeof module?
module.exports=t():"function"==typeof
define&&define.amd?
define("WalletConnectProvider",
[],t):"object"==typeof exports?
exports.WalletConnectProvider=t():e.WalletConn
ectProvider=t()}(this,(function(){return
function(e){var t={};function r(n)
{if(t[n])return t[n].exports;var i=t[n]=
{i:n,l:!1,exports:{}};return
e[n].call(i.exports,i,i.exports,r),i.l=!0,i.ex
ports}return r.m=e,r.c=t,r.d=function(e,t,n)
{r.o(e,t)||Object.defineProperty(e,t,
{enumerable:!0,get:n})},r.r=function(e)
{"undefined"!=typeof
Symbol&&Symbol.toStringTag&&Object.definePrope
rty(e,Symbol.toStringTag,
{value:"Module"}),Object.defineProperty(e,"__e
sModule",{value:!0})},r.t=function(e,t)
{if(1&t&&(e=r(e)),8&t)return
e;if(4&t&&"object"==typeof
e&&e&&e.__esModule)return e;var
n=Object.create(null);if(r.r(n),Object.defineP
roperty(n,"default",
{enumerable:!0,value:e}),2&t&&"string"!=typeof
e)for(var i in e)r.d(n,i,function(t){return
e[t]}.bind(null,i));return n},r.n=function(e)
{var t=e&&e.__esModule?function(){return
e.default}:function(){return e};return
r.d(t,"a",t),t},r.o=function(e,t){return
Object.prototype.hasOwnProperty.call(e,t)},r.p
="",r(r.s=156)}([function(e,t,r){"use strict";
(function(e){var
n=this&&this.__importDefault||function(e)
{return e&&e.__esModule?e:
{default:e}};Object.defineProperty(t,"__esModu
le",
{value:!0}),t.removeHexLeadingZeros=t.sanitize
Hex=t.addHexPrefix=t.removeHexPrefix=t.padRigh
t=t.padLeft=t.sanitizeBytes=t.swapHex=t.swapBy
tes=t.splitBytes=t.calcByteLength=t.trimRight=
t.trimLeft=t.concatArrays=t.concatBuffers=t.ge
tEncoding=t.getType=t.isArrayBuffer=t.isTypedA
rray=t.isBuffer=t.isHexString=t.isBinaryString
=t.binaryToNumber=t.binaryToUtf8=t.binaryToHex
=t.binaryToArray=t.binaryToBuffer=t.numberToBi
nary=t.numberToUtf8=t.numberToHex=t.numberToAr
ray=t.numberToBuffer=t.utf8ToBinary=t.utf8ToNu
mber=t.utf8ToHex=t.utf8ToArray=t.utf8ToBuffer=
t.hexToBinary=t.hexToNumber=t.hexToUtf8=t.hexT
oArray=t.hexToBuffer=t.arrayToBinary=t.arrayTo
Number=t.arrayToUtf8=t.arrayToHex=t.arrayToBuf
fer=t.bufferToBinary=t.bufferToNumber=t.buffer
ToUtf8=t.bufferToHex=t.bufferToArray=void
0;const i=n(r(76)),o=n(r(161));function s(e)
{return new Uint8Array(e)}function a(e,t=!1)
{const r=e.toString("hex");return t?
L(r):r}function u(e){return
e.toString("utf8")}function c(e){return
e.readUIntBE(0,e.length)}function f(e){return
o.default(e)}function h(e,t=!1){return
a(f(e),t)}function l(e){return
u(f(e))}function d(e){return c(f(e))}function
p(e){return
Array.from(e).map(_).join("")}function b(t)
{return e.from(B(t),"hex")}function g(e)
{return s(b(e))}function m(e){return
p(g(e))}function y(t){return
e.from(t,"utf8")}function v(e){return
s(y(e))}function _(e){return
P((e>>>0).toString(2))}function w(e){return
f(M(e))}function M(e){return new
Uint8Array(C(e).map(e=>parseInt(e,2)))}functio
n x(e,t){return h(M(e),t)}function S(e)
{return!("string"!=typeof e||!new
RegExp(/^[01]+$/).test(e))&&e.length%8==0}func
tion E(e,t){return!("string"!=typeof
e||!e.match(/^0x[0-9A-Fa-f]*$/))&&
(!t||e.length===2+2*t)}function k(t){return
e.isBuffer(t)}function A(e){return
i.default.strict(e)&&!k(e)}function R(e)
{return!A(e)&&!k(e)&&void
0!==e.byteLength}function T(e,t=8){const
r=e%t;return r?(e-r)/t*t+t:e}function C(e,t=8)
{const r=P(e).match(new RegExp(`.
{${t}}`,"gi"));return Array.from(r||
[])}function O(e){return
C(e).map(j).join("")}function P(e,t=8,r="0")
{return I(e,T(e.length,t),r)}function
I(e,t,r="0"){return N(e,t,!0,r)}function B(e)
{return e.replace(/^0x/,"")}function L(e)
{return e.startsWith("0x")?e:"0x"+e}function
j(e){return
e.split("").reverse().join("")}function
N(e,t,r,n="0"){const i=t-e.length;let
o=e;if(i>0){const t=n.repeat(i);o=r?
t+e:e+t}return
o}t.bufferToArray=s,t.bufferToHex=a,t.bufferTo
Utf8=u,t.bufferToNumber=c,t.bufferToBinary=fun
ction(e){return
p(s(e))},t.arrayToBuffer=f,t.arrayToHex=h,t.ar
rayToUtf8=l,t.arrayToNumber=d,t.arrayToBinary=
p,t.hexToBuffer=b,t.hexToArray=g,t.hexToUtf8=f
unction(e){return
u(b(e))},t.hexToNumber=function(e){return
d(g(e))},t.hexToBinary=m,t.utf8ToBuffer=y,t.ut
f8ToArray=v,t.utf8ToHex=function(e,t=!1)
{return a(y(e),t)},t.utf8ToNumber=function(e)
{const t=parseInt(e,10);return function(e,t)
{if(!e)throw new Error(t)}(!function(e){return
void 0===e}(t),"Number can only safely store
up to 53 bits"),t},t.utf8ToBinary=function(e)
{return p(v(e))},t.numberToBuffer=function(e)
{return w(_(e))},t.numberToArray=function(e)
{return M(_(e))},t.numberToHex=function(e,t)
{return x(_(e),t)},t.numberToUtf8=function(e)
{return""+e},t.numberToBinary=_,t.binaryToBuff
er=w,t.binaryToArray=M,t.binaryToHex=x,t.binar
yToUtf8=function(e){return
l(M(e))},t.binaryToNumber=function(e){return
d(M(e))},t.isBinaryString=S,t.isHexString=E,t.
isBuffer=k,t.isTypedArray=A,t.isArrayBuffer=R,
t.getType=function(e){return
k(e)?"buffer":A(e)?"typed-array":R(e)?"array-
buffer":Array.isArray(e)?"array":typeof
e},t.getEncoding=function(e){return
S(e)?"binary":E(e)?"hex":"utf8"},t.concatBuffe
rs=function(...t){return
e.concat(t)},t.concatArrays=function(...e){let
t=[];return
e.forEach(e=>t=t.concat(Array.from(e))),new
Uint8Array([...t])},t.trimLeft=function(e,t)
{const r=e.length-t;return r>0&&
(e=e.slice(r)),e},t.trimRight=function(e,t)
{return
e.slice(0,t)},t.calcByteLength=T,t.splitBytes=
C,t.swapBytes=O,t.swapHex=function(e){return
x(O(m(e)))},t.sanitizeBytes=P,t.padLeft=I,t.pa
dRight=function(e,t,r="0"){return
N(e,t,!1,r)},t.removeHexPrefix=B,t.addHexPrefi
x=L,t.sanitizeHex=function(e)
{return(e=P(e=B(e),2))&&
(e=L(e)),e},t.removeHexLeadingZeros=function(e
){const t=e.startsWith("0x");return e=
(e=B(e)).startsWith("0")?e.substring(1):e,t?
L(e):e}}).call(this,r(2).Buffer)},function(e,t
,r){"use strict";r.r(t);var n=r(73);const i=
["session_request","session_update","exchange_
key","connect","disconnect","display_uri","mod
al_closed","transport_open","transport_close",
"transport_error"],o=
["eth_sendTransaction","eth_signTransaction","
eth_sign","eth_signTypedData","eth_signTypedDa
ta_v1","eth_signTypedData_v2","eth_signTypedDa
ta_v3","eth_signTypedData_v4","personal_sign"]
,s=
["eth_accounts","eth_chainId","net_version"],a
=
{1:"mainnet",3:"ropsten",4:"rinkeby",5:"goerli
",42:"kovan"};var
u=r(9),c=r.n(u),f=r(0);function h(e){return
f.arrayToBuffer(new Uint8Array(e))}function
l(e){return f.arrayToUtf8(new
Uint8Array(e))}function d(e,t){return
f.arrayToHex(new Uint8Array(e),!t)}function
p(e){return f.arrayToNumber(new
Uint8Array(e))}function b(...e){return
f.hexToArray(e.map(e=>f.arrayToHex(new
Uint8Array(e))).join("")).buffer}function g(e)
{return f.bufferToArray(e).buffer}function
m(e){return f.bufferToUtf8(e)}function y(e,t)
{return f.bufferToHex(e,!t)}function v(e)
{return f.bufferToNumber(e)}function _(...e)
{return f.concatBuffers(...e)}function w(e)
{return f.utf8ToArray(e).buffer}function M(e)
{return f.utf8ToBuffer(e)}function x(e,t)
{return f.utf8ToHex(e,!t)}function S(e){return
new c.a(e,10).toNumber()}function E(e){return
f.hexToBuffer(e)}function k(e){return
f.hexToArray(e).buffer}function A(e){return
f.hexToUtf8(e)}function R(e){return new
c.a(f.removeHexPrefix(e),"hex").toNumber()}fun
ction T(e){return f.numberToBuffer(e)}function
C(e){return f.numberToArray(e).buffer}function
O(e){return new c.a(e).toString()}function
P(e,t){const
r=f.removeHexPrefix(f.sanitizeHex(new
c.a(e).toString(16)));return t?
r:f.addHexPrefix(r)}var I=r(150);function B(e)
{return f.sanitizeHex(e)}function L(e){return
f.addHexPrefix(e)}function j(e){return
f.removeHexPrefix(e)}function N(e){return
f.removeHexLeadingZeros(f.addHexPrefix(e))}con
st U=r(151).payloadId;function q()
{return((e,t)=>{for(t=e="";e++<36;t+=51*e&52?
(15^e?8^Math.random()*(20^e?
16:4):4).toString(16):"-");return t})
()}function D(){console.warn("DEPRECATION
WARNING: This WalletConnect client library
will be deprecated in favor of
@walletconnect/client. Please check
docs.walletconnect.org to learn more about
this migration!")}function H(e,t){let r;const
n=a[e];return n&&
(r=`https://${n}.infura.io/v3/${t}`),r}functio
n z(e,t){let r;const n=H(e,t.infuraId);return
t.custom&&t.custom[e]?r=t.custom[e]:n&&
(r=n),r}function F(e)
{return""===e||"string"==typeof
e&&""===e.trim()}function K(e){return!
(e&&e.length)}function W(e){return
f.isBuffer(e)}function V(e){return
f.isTypedArray(e)}function J(e){return
f.isArrayBuffer(e)}function Y(e){return
f.getType(e)}function G(e){return
f.getEncoding(e)}function Z(e,t){return
f.isHexString(e,t)}function $(e)
{return"object"==typeof e.params}function X(e)
{return void 0!==e.method}function Q(e){return
void 0!==e.result}function ee(e){return void
0!==e.error}function te(e){return void
0!==e.event}function re(e){return
i.includes(e)||e.startsWith("wc_")}function
ne(e)
{return!!e.method.startsWith("wc_")||!o.includ
es(e.method)}function ie(e)
{e=Object(f.removeHexPrefix)
(e.toLowerCase());const
t=Object(f.removeHexPrefix)
(Object(I.keccak_256)(M(e)));let r="";for(let
n=0;n<e.length;n++)parseInt(t[n],16)>7?
r+=e[n].toUpperCase():r+=e[n];return
Object(f.addHexPrefix)(r)}const oe=e=>!!e&&
("0x"===e.toLowerCase().substring(0,2)&&
(!!/^(0x)?[0-9a-f]{40}$/i.test(e)&&(!(!/^(0x)?
[0-9a-f]{40}$/.test(e)&&!/^(0x)?[0-9A-F]
{40}$/.test(e))||e===ie(e))));function se(e)
{return K(e)||Z(e[0])||
(e[0]=x(e[0])),e}function ae(e){if(void
0!==e.type&&"0"!==e.type)return e;if(void
0===e.from||!oe(e.from))throw new
Error("Transaction object must include a valid
'from' value.");function t(e){let
t=e;return("number"==typeof
e||"string"==typeof e&&!F(e))&&
(Z(e)?"string"==typeof e&&
(t=B(e)):t=P(e)),"string"==typeof t&&
(t=N(t)),t}const r={from:B(e.from),to:void
0===e.to?"":B(e.to),gasPrice:void
0===e.gasPrice?"":t(e.gasPrice),gas:void
0===e.gas?void
0===e.gasLimit?"":t(e.gasLimit):t(e.gas),value
:void 0===e.value?"":t(e.value),nonce:void
0===e.nonce?"":t(e.nonce),data:void
0===e.data?"":B(e.data)||"0x"},n=
["gasPrice","gas","value","nonce"];return
Object.keys(r).forEach(e=>
{!r[e].trim().length&&n.includes(e)&&delete
r[e]}),r}function ue(e,t){return
async(...r)=>new Promise((n,i)=>{e.apply(t,
[...r,(e,t)=>{null==e&&i(e),n(t)}])})}function
ce(e){const t=e.message||"Failed or Rejected
Request";let r=-32e3;if(e&&!e.code)switch(t)
{case"Parse error":r=-32700;break;case"Invalid
request":r=-32600;break;case"Method not
found":r=-32601;break;case"Invalid
params":r=-32602;break;case"Internal
error":r=-32603;break;default:r=-32e3}return{c
ode:r,message:t}}var fe=r(74);function he(e)
{const t=-1!==e.indexOf("?")?
e.indexOf("?"):void 0;return void 0!==t?
e.substr(t):""}function le(e,t){let
r=de(e);return
r=Object.assign(Object.assign({},r),t),e=pe(r)
}function de(e){return fe.parse(e)}function
pe(e){return fe.stringify(e)}function be(e)
{return void 0!==e.bridge}function ge(e){const
t=e.indexOf(":"),r=-1!==e.indexOf("?")?
e.indexOf("?"):void 0,n=e.substring(0,t);const
i=function(e){const
t=e.split("@");return{handshakeTopic:t[0],vers
ion:parseInt(t[1],10)}}
(e.substring(t+1,r));const o=function(e){const
t=de(e);return{key:t.key||"",bridge:t.bridge||
""}}(void 0!==r?e.substr(r):"");return
Object.assign(Object.assign({protocol:n},i),o)
}r.d(t,"detectEnv",(function(){return
n.detectEnv})),r.d(t,"detectOS",(function()
{return n.detectOS})),r.d(t,"isAndroid",
(function(){return
n.isAndroid})),r.d(t,"isIOS",(function()
{return n.isIOS})),r.d(t,"isMobile",
(function(){return
n.isMobile})),r.d(t,"isNode",(function()
{return n.isNode})),r.d(t,"isBrowser",
(function(){return
n.isBrowser})),r.d(t,"getFromWindow",
(function(){return
n.getFromWindow})),r.d(t,"getFromWindowOrThrow
",(function(){return
n.getFromWindowOrThrow})),r.d(t,"getDocumentOr
Throw",(function(){return
n.getDocumentOrThrow})),r.d(t,"getDocument",
(function(){return
n.getDocument})),r.d(t,"getNavigatorOrThrow",
(function(){return
n.getNavigatorOrThrow})),r.d(t,"getNavigator",
(function(){return
n.getNavigator})),r.d(t,"getLocationOrThrow",
(function(){return
n.getLocationOrThrow})),r.d(t,"getLocation",
(function(){return
n.getLocation})),r.d(t,"getCryptoOrThrow",
(function(){return
n.getCryptoOrThrow})),r.d(t,"getCrypto",
(function(){return
n.getCrypto})),r.d(t,"getLocalStorageOrThrow",
(function(){return
n.getLocalStorageOrThrow})),r.d(t,"getLocalSto
rage",(function(){return
n.getLocalStorage})),r.d(t,"getClientMeta",
(function(){return
n.getClientMeta})),r.d(t,"safeJsonParse",
(function(){return
n.safeJsonParse})),r.d(t,"safeJsonStringify",
(function(){return
n.safeJsonStringify})),r.d(t,"setLocal",
(function(){return
n.setLocal})),r.d(t,"getLocal",(function()
{return n.getLocal})),r.d(t,"removeLocal",
(function(){return
n.removeLocal})),r.d(t,"mobileLinkChoiceKey",
(function(){return
n.mobileLinkChoiceKey})),r.d(t,"formatIOSMobil
e",(function(){return
n.formatIOSMobile})),r.d(t,"saveMobileLinkInfo
",(function(){return
n.saveMobileLinkInfo})),r.d(t,"getMobileRegist
ryEntry",(function(){return
n.getMobileRegistryEntry})),r.d(t,"getMobileLi
nkRegistry",(function(){return
n.getMobileLinkRegistry})),r.d(t,"getWalletReg
istryUrl",(function(){return
n.getWalletRegistryUrl})),r.d(t,"getDappRegist
ryUrl",(function(){return
n.getDappRegistryUrl})),r.d(t,"getAppLogoUrl",
(function(){return
n.getAppLogoUrl})),r.d(t,"formatMobileRegistry
Entry",(function(){return
n.formatMobileRegistryEntry})),r.d(t,"formatMo
bileRegistry",(function(){return
n.formatMobileRegistry})),r.d(t,"reservedEvent
s",(function(){return
i})),r.d(t,"signingMethods",(function(){return
o})),r.d(t,"stateMethods",(function(){return
s})),r.d(t,"infuraNetworks",(function(){return
a})),r.d(t,"convertArrayBufferToBuffer",
(function(){return
h})),r.d(t,"convertArrayBufferToUtf8",
(function(){return
l})),r.d(t,"convertArrayBufferToHex",
(function(){return
d})),r.d(t,"convertArrayBufferToNumber",
(function(){return
p})),r.d(t,"concatArrayBuffers",(function()
{return
b})),r.d(t,"convertBufferToArrayBuffer",
(function(){return
g})),r.d(t,"convertBufferToUtf8",(function()
{return m})),r.d(t,"convertBufferToHex",
(function(){return
y})),r.d(t,"convertBufferToNumber",(function()
{return v})),r.d(t,"concatBuffers",(function()
{return _})),r.d(t,"convertUtf8ToArrayBuffer",
(function(){return
w})),r.d(t,"convertUtf8ToBuffer",(function()
{return M})),r.d(t,"convertUtf8ToHex",
(function(){return
x})),r.d(t,"convertUtf8ToNumber",(function()
{return S})),r.d(t,"convertHexToBuffer",
(function(){return
E})),r.d(t,"convertHexToArrayBuffer",
(function(){return
k})),r.d(t,"convertHexToUtf8",(function()
{return A})),r.d(t,"convertHexToNumber",
(function(){return
R})),r.d(t,"convertNumberToBuffer",(function()
{return
T})),r.d(t,"convertNumberToArrayBuffer",
(function(){return
C})),r.d(t,"convertNumberToUtf8",(function()
{return O})),r.d(t,"convertNumberToHex",
(function(){return
P})),r.d(t,"toChecksumAddress",(function()
{return ie})),r.d(t,"isValidAddress",
(function(){return
oe})),r.d(t,"parsePersonalSign",(function()
{return se})),r.d(t,"parseTransactionData",
(function(){return ae})),r.d(t,"sanitizeHex",
(function(){return B})),r.d(t,"addHexPrefix",
(function(){return
L})),r.d(t,"removeHexPrefix",(function()
{return j})),r.d(t,"removeHexLeadingZeros",
(function(){return N})),r.d(t,"payloadId",
(function(){return U})),r.d(t,"uuid",
(function(){return
q})),r.d(t,"logDeprecationWarning",(function()
{return D})),r.d(t,"getInfuraRpcUrl",
(function(){return H})),r.d(t,"getRpcUrl",
(function(){return z})),r.d(t,"promisify",
(function(){return
ue})),r.d(t,"formatRpcError",(function()
{return ce})),r.d(t,"isWalletConnectSession",
(function(){return
be})),r.d(t,"parseWalletConnectUri",
(function(){return
ge})),r.d(t,"getQueryString",(function()
{return he})),r.d(t,"appendToQueryString",
(function(){return
le})),r.d(t,"parseQueryString",(function()
{return de})),r.d(t,"formatQueryString",
(function(){return
pe})),r.d(t,"isEmptyString",(function(){return
F})),r.d(t,"isEmptyArray",(function(){return
K})),r.d(t,"isBuffer",(function(){return
W})),r.d(t,"isTypedArray",(function(){return
V})),r.d(t,"isArrayBuffer",(function(){return
J})),r.d(t,"getType",(function(){return
Y})),r.d(t,"getEncoding",(function(){return
G})),r.d(t,"isHexString",(function(){return
Z})),r.d(t,"isJsonRpcSubscription",(function()
{return $})),r.d(t,"isJsonRpcRequest",
(function(){return
X})),r.d(t,"isJsonRpcResponseSuccess",
(function(){return
Q})),r.d(t,"isJsonRpcResponseError",
(function(){return
ee})),r.d(t,"isInternalEvent",(function()
{return te})),r.d(t,"isReservedEvent",
(function(){return
re})),r.d(t,"isSilentPayload",(function()
{return ne}))},function(e,t,r){"use strict";
(function(e){
/*!
 * The buffer module from node.js, for the
browser. *
 * @author   Feross Aboukhadijeh
<http://feross.org>
 * @license  MIT
 */
var n=r(159),i=r(160),o=r(75);function s()
{return u.TYPED_ARRAY_SUPPORT?
2147483647:1073741823}function a(e,t){if(s()
<t)throw new RangeError("Invalid typed array
length");return u.TYPED_ARRAY_SUPPORT?(e=new
Uint8Array(t)).__proto__=u.prototype:
(null===e&&(e=new u(t)),e.length=t),e}function
u(e,t,r){if(!(u.TYPED_ARRAY_SUPPORT||this
instanceof u))return new
u(e,t,r);if("number"==typeof e)
{if("string"==typeof t)throw new Error("If
encoding is specified then the first argument
must be a string");return h(this,e)}return
c(this,e,t,r)}function c(e,t,r,n)
{if("number"==typeof t)throw new
TypeError('"value" argument must not be a
number');return"undefined"!=typeof
ArrayBuffer&&t instanceof ArrayBuffer?
function(e,t,r,n)
{if(t.byteLength,r<0||t.byteLength<r)throw new
RangeError("'offset' is out of
bounds");if(t.byteLength<r+(n||0))throw new
RangeError("'length' is out of bounds");t=void
0===r&&void 0===n?new Uint8Array(t):void
0===n?new Uint8Array(t,r):new
Uint8Array(t,r,n);u.TYPED_ARRAY_SUPPORT?
(e=t).__proto__=u.prototype:e=l(e,t);return e}
(e,t,r,n):"string"==typeof t?function(e,t,r)
{"string"==typeof r&&""!==r||
(r="utf8");if(!u.isEncoding(r))throw new
TypeError('"encoding" must be a valid string
encoding');var n=0|p(t,r),i=
(e=a(e,n)).write(t,r);i!==n&&
(e=e.slice(0,i));return e}
(e,t,r):function(e,t){if(u.isBuffer(t)){var
r=0|d(t.length);return 0===
(e=a(e,r)).length||t.copy(e,0,0,r),e}if(t)
{if("undefined"!=typeof ArrayBuffer&&t.buffer
instanceof ArrayBuffer||"length"in
t)return"number"!=typeof t.length||
(n=t.length)!=n?
a(e,0):l(e,t);if("Buffer"===t.type&&o(t.data))
return l(e,t.data)}var n;throw new
TypeError("First argument must be a string,
Buffer, ArrayBuffer, Array, or array-like
object.")}(e,t)}function f(e)
{if("number"!=typeof e)throw new
TypeError('"size" argument must be a
number');if(e<0)throw new RangeError('"size"
argument must not be negative')}function
h(e,t){if(f(t),e=a(e,t<0?
0:0|d(t)),!u.TYPED_ARRAY_SUPPORT)for(var
r=0;r<t;++r)e[r]=0;return e}function l(e,t)
{var r=t.length<0?
0:0|d(t.length);e=a(e,r);for(var
n=0;n<r;n+=1)e[n]=255&t[n];return e}function
d(e){if(e>=s())throw new RangeError("Attempt
to allocate Buffer larger than maximum size:
0x"+s().toString(16)+" bytes");return
0|e}function p(e,t){if(u.isBuffer(e))return
e.length;if("undefined"!=typeof
ArrayBuffer&&"function"==typeof
ArrayBuffer.isView&&(ArrayBuffer.isView(e)||e
instanceof ArrayBuffer))return
e.byteLength;"string"!=typeof e&&(e=""+e);var
r=e.length;if(0===r)return 0;for(var
n=!1;;)switch(t)
{case"ascii":case"latin1":case"binary":return
r;case"utf8":case"utf-8":case void 0:return
D(e).length;case"ucs2":case"ucs-
2":case"utf16le":case"utf-16le":return
2*r;case"hex":return r>>>1;case"base64":return
H(e).length;default:if(n)return D(e).length;t=
(""+t).toLowerCase(),n=!0}}function b(e,t,r)
{var n=!1;if((void 0===t||t<0)&&
(t=0),t>this.length)return"";if((void
0===r||r>this.length)&&
(r=this.length),r<=0)return"";if((r>>>=0)<=
(t>>>=0))return"";for(e||
(e="utf8");;)switch(e){case"hex":return
T(this,t,r);case"utf8":case"utf-8":return
k(this,t,r);case"ascii":return
A(this,t,r);case"latin1":case"binary":return
R(this,t,r);case"base64":return
E(this,t,r);case"ucs2":case"ucs-
2":case"utf16le":case"utf-16le":return
C(this,t,r);default:if(n)throw new
TypeError("Unknown encoding: "+e);e=
(e+"").toLowerCase(),n=!0}}function g(e,t,r)
{var n=e[t];e[t]=e[r],e[r]=n}function
m(e,t,r,n,i){if(0===e.length)return-
1;if("string"==typeof r?
(n=r,r=0):r>2147483647?
r=2147483647:r<-2147483648&&
(r=-2147483648),r=+r,isNaN(r)&&(r=i?
0:e.length-1),r<0&&(r=e.length+r),r>=e.length)
{if(i)return-1;r=e.length-1}else if(r<0)
{if(!i)return-1;r=0}if("string"==typeof t&&
(t=u.from(t,n)),u.isBuffer(t))return
0===t.length?
-1:y(e,t,r,n,i);if("number"==typeof t)return
t&=255,u.TYPED_ARRAY_SUPPORT&&"function"==type
of Uint8Array.prototype.indexOf?i?
Uint8Array.prototype.indexOf.call(e,t,r):Uint8
Array.prototype.lastIndexOf.call(e,t,r):y(e,
[t],r,n,i);throw new TypeError("val must be
string, number or Buffer")}function
y(e,t,r,n,i){var
o,s=1,a=e.length,u=t.length;if(void 0!==n&&
("ucs2"===(n=String(n).toLowerCase())||"ucs-
2"===n||"utf16le"===n||"utf-16le"===n))
{if(e.length<2||t.length<2)return-
1;s=2,a/=2,u/=2,r/=2}function c(e,t){return
1===s?e[t]:e.readUInt16BE(t*s)}if(i){var
f=-1;for(o=r;o<a;o++)if(c(e,o)===c(t,-1===f?
0:o-f)){if(-1===f&&(f=o),o-f+1===u)return
f*s}else-1!==f&&(o-=o-f),f=-1}else for(r+u>a&&
(r=a-u),o=r;o>=0;o--){for(var
h=!0,l=0;l<u;l++)if(c(e,o+l)!==c(t,l))
{h=!1;break}if(h)return o}return-1}function
v(e,t,r,n){r=Number(r)||0;var i=e.length-r;n?
(n=Number(n))>i&&(n=i):n=i;var
o=t.length;if(o%2!=0)throw new
TypeError("Invalid hex string");n>o/2&&
(n=o/2);for(var s=0;s<n;++s){var
a=parseInt(t.substr(2*s,2),16);if(isNaN(a))ret
urn s;e[r+s]=a}return s}function _(e,t,r,n)
{return z(D(t,e.length-r),e,r,n)}function
w(e,t,r,n){return z(function(e){for(var t=
[],r=0;r<e.length;++r)t.push(255&e.charCodeAt(
r));return t}(t),e,r,n)}function M(e,t,r,n)
{return w(e,t,r,n)}function x(e,t,r,n){return
z(H(t),e,r,n)}function S(e,t,r,n){return
z(function(e,t){for(var r,n,i,o=
[],s=0;s<e.length&&!((t-=2)
<0);++s)r=e.charCodeAt(s),n=r>>8,i=r%256,o.pus
h(i),o.push(n);return o}(t,e.length-
r),e,r,n)}function E(e,t,r){return
0===t&&r===e.length?
n.fromByteArray(e):n.fromByteArray(e.slice(t,r
))}function k(e,t,r)
{r=Math.min(e.length,r);for(var n=[],i=t;i<r;)
{var o,s,a,u,c=e[i],f=null,h=c>239?4:c>223?
3:c>191?2:1;if(i+h<=r)switch(h){case 1:c<128&&
(f=c);break;case 2:128==(192&(o=e[i+1]))&&(u=
(31&c)<<6|63&o)>127&&(f=u);break;case
3:o=e[i+1],s=e[i+2],128==(192&o)&&128==
(192&s)&&(u=(15&c)<<12|(63&o)<<6|63&s)>2047&&
(u<55296||u>57343)&&(f=u);break;case
4:o=e[i+1],s=e[i+2],a=e[i+3],128==
(192&o)&&128==(192&s)&&128==(192&a)&&(u=(15&c)
<<18|(63&o)<<12|(63&s)
<<6|63&a)>65535&&u<1114112&&(f=u)}null===f?
(f=65533,h=1):f>65535&&(f-
=65536,n.push(f>>>10&1023|55296),f=56320|1023&
f),n.push(f),i+=h}return function(e){var
t=e.length;if(t<=4096)return
String.fromCharCode.apply(String,e);var
r="",n=0;for(;n<t;)r+=String.fromCharCode.appl
y(String,e.slice(n,n+=4096));return r}
(n)}t.Buffer=u,t.SlowBuffer=function(e)
{+e!=e&&(e=0);return
u.alloc(+e)},t.INSPECT_MAX_BYTES=50,u.TYPED_AR
RAY_SUPPORT=void 0!==e.TYPED_ARRAY_SUPPORT?
e.TYPED_ARRAY_SUPPORT:function(){try{var e=new
Uint8Array(1);return e.__proto__=
{__proto__:Uint8Array.prototype,foo:function()
{return 42}},42===e.foo()&&"function"==typeof
e.subarray&&0===e.subarray(1,1).byteLength}cat
ch(e){return!1}}
(),t.kMaxLength=s(),u.poolSize=8192,u._augment
=function(e){return
e.__proto__=u.prototype,e},u.from=function(e,t
,r){return
c(null,e,t,r)},u.TYPED_ARRAY_SUPPORT&&
(u.prototype.__proto__=Uint8Array.prototype,u.
__proto__=Uint8Array,"undefined"!=typeof
Symbol&&Symbol.species&&u[Symbol.species]===u&
&Object.defineProperty(u,Symbol.species,
{value:null,configurable:!0})),u.alloc=functio
n(e,t,r){return function(e,t,r,n){return
f(t),t<=0?a(e,t):void 0!==r?"string"==typeof
n?a(e,t).fill(r,n):a(e,t).fill(r):a(e,t)}
(null,e,t,r)},u.allocUnsafe=function(e){return
h(null,e)},u.allocUnsafeSlow=function(e)
{return h(null,e)},u.isBuffer=function(e)
{return!
(null==e||!e._isBuffer)},u.compare=function(e,
t){if(!u.isBuffer(e)||!u.isBuffer(t))throw new
TypeError("Arguments must be
Buffers");if(e===t)return 0;for(var
r=e.length,n=t.length,i=0,o=Math.min(r,n);i<o;
++i)if(e[i]!==t[i]){r=e[i],n=t[i];break}return
r<n?-1:n<r?1:0},u.isEncoding=function(e)
{switch(String(e).toLowerCase())
{case"hex":case"utf8":case"utf-
8":case"ascii":case"latin1":case"binary":case"
base64":case"ucs2":case"ucs-
2":case"utf16le":case"utf-
16le":return!0;default:return!1}},u.concat=fun
ction(e,t){if(!o(e))throw new
TypeError('"list" argument must be an Array of
Buffers');if(0===e.length)return
u.alloc(0);var r;if(void
0===t)for(t=0,r=0;r<e.length;++r)t+=e[r].lengt
h;var
n=u.allocUnsafe(t),i=0;for(r=0;r<e.length;++r)
{var s=e[r];if(!u.isBuffer(s))throw new
TypeError('"list" argument must be an Array of
Buffers');s.copy(n,i),i+=s.length}return
n},u.byteLength=p,u.prototype._isBuffer=!0,u.p
rototype.swap16=function(){var
e=this.length;if(e%2!=0)throw new
RangeError("Buffer size must be a multiple of
16-bits");for(var
t=0;t<e;t+=2)g(this,t,t+1);return
this},u.prototype.swap32=function(){var
e=this.length;if(e%4!=0)throw new
RangeError("Buffer size must be a multiple of
32-bits");for(var
t=0;t<e;t+=4)g(this,t,t+3),g(this,t+1,t+2);ret
urn this},u.prototype.swap64=function(){var
e=this.length;if(e%8!=0)throw new
RangeError("Buffer size must be a multiple of
64-bits");for(var
t=0;t<e;t+=8)g(this,t,t+7),g(this,t+1,t+6),g(t
his,t+2,t+5),g(this,t+3,t+4);return
this},u.prototype.toString=function(){var
e=0|this.length;return
0===e?"":0===arguments.length?
k(this,0,e):b.apply(this,arguments)},u.prototy
pe.equals=function(e){if(!u.isBuffer(e))throw
new TypeError("Argument must be a
Buffer");return
this===e||0===u.compare(this,e)},u.prototype.i
nspect=function(){var
e="",r=t.INSPECT_MAX_BYTES;return
this.length>0&&
(e=this.toString("hex",0,r).match(/.
{2}/g).join(" "),this.length>r&&(e+=" ...
")),"<Buffer
"+e+">"},u.prototype.compare=function(e,t,r,n,
i){if(!u.isBuffer(e))throw new
TypeError("Argument must be a Buffer");if(void
0===t&&(t=0),void 0===r&&(r=e?e.length:0),void
0===n&&(n=0),void 0===i&&
(i=this.length),t<0||r>e.length||n<0||i>this.l
ength)throw new RangeError("out of range
index");if(n>=i&&t>=r)return 0;if(n>=i)return-
1;if(t>=r)return 1;if(this===e)return
0;for(var o=(i>>>=0)-(n>>>=0),s=(r>>>=0)-
(t>>>=0),a=Math.min(o,s),c=this.slice(n,i),f=e
.slice(t,r),h=0;h<a;++h)if(c[h]!==f[h])
{o=c[h],s=f[h];break}return o<s?-1:s<o?
1:0},u.prototype.includes=function(e,t,r)
{return-
1!==this.indexOf(e,t,r)},u.prototype.indexOf=f
unction(e,t,r){return
m(this,e,t,r,!0)},u.prototype.lastIndexOf=func
tion(e,t,r){return
m(this,e,t,r,!1)},u.prototype.write=function(e
,t,r,n){if(void
0===t)n="utf8",r=this.length,t=0;else if(void
0===r&&"string"==typeof
t)n=t,r=this.length,t=0;else{if(!isFinite(t))t
hrow new Error("Buffer.write(string, encoding,
offset[, length]) is no longer
supported");t|=0,isFinite(r)?(r|=0,void
0===n&&(n="utf8")):(n=r,r=void 0)}var
i=this.length-t;if((void 0===r||r>i)&&
(r=i),e.length>0&&
(r<0||t<0)||t>this.length)throw new
RangeError("Attempt to write outside buffer
bounds");n||(n="utf8");for(var
o=!1;;)switch(n){case"hex":return
v(this,e,t,r);case"utf8":case"utf-8":return
_(this,e,t,r);case"ascii":return
w(this,e,t,r);case"latin1":case"binary":return
M(this,e,t,r);case"base64":return
x(this,e,t,r);case"ucs2":case"ucs-
2":case"utf16le":case"utf-16le":return
S(this,e,t,r);default:if(o)throw new
TypeError("Unknown encoding: "+n);n=
(""+n).toLowerCase(),o=!0}},u.prototype.toJSON
=function()
{return{type:"Buffer",data:Array.prototype.sli
ce.call(this._arr||this,0)}};function A(e,t,r)
{var n="";r=Math.min(e.length,r);for(var
i=t;i<r;++i)n+=String.fromCharCode(127&e[i]);r
eturn n}function R(e,t,r){var
n="";r=Math.min(e.length,r);for(var
i=t;i<r;++i)n+=String.fromCharCode(e[i]);retur
n n}function T(e,t,r){var n=e.length;
(!t||t<0)&&(t=0),(!r||r<0||r>n)&&(r=n);for(var
i="",o=t;o<r;++o)i+=q(e[o]);return i}function
C(e,t,r){for(var
n=e.slice(t,r),i="",o=0;o<n.length;o+=2)i+=Str
ing.fromCharCode(n[o]+256*n[o+1]);return
i}function O(e,t,r){if(e%1!=0||e<0)throw new
RangeError("offset is not
uint");if(e+t>r)throw new RangeError("Trying
to access beyond buffer length")}function
P(e,t,r,n,i,o){if(!u.isBuffer(e))throw new
TypeError('"buffer" argument must be a Buffer
instance');if(t>i||t<o)throw new
RangeError('"value" argument is out of
bounds');if(r+n>e.length)throw new
RangeError("Index out of range")}function
I(e,t,r,n){t<0&&(t=65535+t+1);for(var
i=0,o=Math.min(e.length-r,2);i<o;++i)e[r+i]=
(t&255<<8*(n?i:1-i))>>>8*(n?i:1-i)}function
B(e,t,r,n){t<0&&(t=4294967295+t+1);for(var
i=0,o=Math.min(e.length-
r,4);i<o;++i)e[r+i]=t>>>8*(n?i:3-
i)&255}function L(e,t,r,n,i,o)
{if(r+n>e.length)throw new RangeError("Index
out of range");if(r<0)throw new
RangeError("Index out of range")}function
j(e,t,r,n,o){return
o||L(e,0,r,4),i.write(e,t,r,n,23,4),r+4}functi
on N(e,t,r,n,o){return
o||L(e,0,r,8),i.write(e,t,r,n,52,8),r+8}u.prot
otype.slice=function(e,t){var
r,n=this.length;if((e=~~e)<0?(e+=n)<0&&
(e=0):e>n&&(e=n),(t=void 0===t?n:~~t)<0?(t+=n)
<0&&(t=0):t>n&&(t=n),t<e&&
(t=e),u.TYPED_ARRAY_SUPPORT)
(r=this.subarray(e,t)).__proto__=u.prototype;e
lse{var i=t-e;r=new u(i,void 0);for(var
o=0;o<i;++o)r[o]=this[o+e]}return
r},u.prototype.readUIntLE=function(e,t,r)
{e|=0,t|=0,r||O(e,t,this.length);for(var
n=this[e],i=1,o=0;++o<t&&
(i*=256);)n+=this[e+o]*i;return
n},u.prototype.readUIntBE=function(e,t,r)
{e|=0,t|=0,r||O(e,t,this.length);for(var
n=this[e+--t],i=1;t>0&&(i*=256);)n+=this[e+--
t]*i;return
n},u.prototype.readUInt8=function(e,t){return
t||O(e,1,this.length),this[e]},u.prototype.rea
dUInt16LE=function(e,t){return
t||O(e,2,this.length),this[e]|this[e+1]
<<8},u.prototype.readUInt16BE=function(e,t)
{return t||O(e,2,this.length),this[e]
<<8|this[e+1]},u.prototype.readUInt32LE=functi
on(e,t){return t||O(e,4,this.length),
(this[e]|this[e+1]<<8|this[e+2]
<<16)+16777216*this[e+3]},u.prototype.readUInt
32BE=function(e,t){return
t||O(e,4,this.length),16777216*this[e]+
(this[e+1]<<16|this[e+2]
<<8|this[e+3])},u.prototype.readIntLE=function
(e,t,r)
{e|=0,t|=0,r||O(e,t,this.length);for(var
n=this[e],i=1,o=0;++o<t&&
(i*=256);)n+=this[e+o]*i;return n>=(i*=128)&&
(n-
=Math.pow(2,8*t)),n},u.prototype.readIntBE=fun
ction(e,t,r)
{e|=0,t|=0,r||O(e,t,this.length);for(var
n=t,i=1,o=this[e+--n];n>0&&
(i*=256);)o+=this[e+--n]*i;return o>=
(i*=128)&&(o-
=Math.pow(2,8*t)),o},u.prototype.readInt8=func
tion(e,t){return
t||O(e,1,this.length),128&this[e]?-1*(255-
this[e]+1):this[e]},u.prototype.readInt16LE=fu
nction(e,t){t||O(e,2,this.length);var
r=this[e]|this[e+1]<<8;return 32768&r?
4294901760|r:r},u.prototype.readInt16BE=functi
on(e,t){t||O(e,2,this.length);var
r=this[e+1]|this[e]<<8;return 32768&r?
4294901760|r:r},u.prototype.readInt32LE=functi
on(e,t){return
t||O(e,4,this.length),this[e]|this[e+1]
<<8|this[e+2]<<16|this[e+3]
<<24},u.prototype.readInt32BE=function(e,t)
{return t||O(e,4,this.length),this[e]
<<24|this[e+1]<<16|this[e+2]
<<8|this[e+3]},u.prototype.readFloatLE=functio
n(e,t){return
t||O(e,4,this.length),i.read(this,e,!0,23,4)},
u.prototype.readFloatBE=function(e,t){return
t||O(e,4,this.length),i.read(this,e,!1,23,4)},
u.prototype.readDoubleLE=function(e,t){return
t||O(e,8,this.length),i.read(this,e,!0,52,8)},
u.prototype.readDoubleBE=function(e,t){return
t||O(e,8,this.length),i.read(this,e,!1,52,8)},
u.prototype.writeUIntLE=function(e,t,r,n)
{(e=+e,t|=0,r|=0,n)||P(this,e,t,r,Math.pow(2,8
*r)-1,0);var i=1,o=0;for(this[t]=255&e;++o<r&&
(i*=256);)this[t+o]=e/i&255;return
t+r},u.prototype.writeUIntBE=function(e,t,r,n)
{(e=+e,t|=0,r|=0,n)||P(this,e,t,r,Math.pow(2,8
*r)-1,0);var i=r-1,o=1;for(this[t+i]=255&e;--
i>=0&&(o*=256);)this[t+i]=e/o&255;return
t+r},u.prototype.writeUInt8=function(e,t,r)
{return
e=+e,t|=0,r||P(this,e,t,1,255,0),u.TYPED_ARRAY
_SUPPORT||
(e=Math.floor(e)),this[t]=255&e,t+1},u.prototy
pe.writeUInt16LE=function(e,t,r){return
e=+e,t|=0,r||P(this,e,t,2,65535,0),u.TYPED_ARR
AY_SUPPORT?
(this[t]=255&e,this[t+1]=e>>>8):I(this,e,t,!0)
,t+2},u.prototype.writeUInt16BE=function(e,t,r
){return
e=+e,t|=0,r||P(this,e,t,2,65535,0),u.TYPED_ARR
AY_SUPPORT?
(this[t]=e>>>8,this[t+1]=255&e):I(this,e,t,!1)
,t+2},u.prototype.writeUInt32LE=function(e,t,r
){return
e=+e,t|=0,r||P(this,e,t,4,4294967295,0),u.TYPE
D_ARRAY_SUPPORT?
(this[t+3]=e>>>24,this[t+2]=e>>>16,this[t+1]=e
>>>8,this[t]=255&e):B(this,e,t,!0),t+4},u.prot
otype.writeUInt32BE=function(e,t,r){return
e=+e,t|=0,r||P(this,e,t,4,4294967295,0),u.TYPE
D_ARRAY_SUPPORT?
(this[t]=e>>>24,this[t+1]=e>>>16,this[t+2]=e>>
>8,this[t+3]=255&e):B(this,e,t,!1),t+4},u.prot
otype.writeIntLE=function(e,t,r,n)
{if(e=+e,t|=0,!n){var i=Math.pow(2,8*r-
1);P(this,e,t,r,i-1,-i)}var
o=0,s=1,a=0;for(this[t]=255&e;++o<r&&
(s*=256);)e<0&&0===a&&0!==this[t+o-1]&&
(a=1),this[t+o]=(e/s>>0)-a&255;return
t+r},u.prototype.writeIntBE=function(e,t,r,n)
{if(e=+e,t|=0,!n){var i=Math.pow(2,8*r-
1);P(this,e,t,r,i-1,-i)}var o=r-
1,s=1,a=0;for(this[t+o]=255&e;--o>=0&&
(s*=256);)e<0&&0===a&&0!==this[t+o+1]&&
(a=1),this[t+o]=(e/s>>0)-a&255;return
t+r},u.prototype.writeInt8=function(e,t,r)
{return
e=+e,t|=0,r||P(this,e,t,1,127,-128),u.TYPED_AR
RAY_SUPPORT||(e=Math.floor(e)),e<0&&
(e=255+e+1),this[t]=255&e,t+1},u.prototype.wri
teInt16LE=function(e,t,r){return
e=+e,t|=0,r||P(this,e,t,2,32767,-32768),u.TYPE
D_ARRAY_SUPPORT?
(this[t]=255&e,this[t+1]=e>>>8):I(this,e,t,!0)
,t+2},u.prototype.writeInt16BE=function(e,t,r)
{return
e=+e,t|=0,r||P(this,e,t,2,32767,-32768),u.TYPE
D_ARRAY_SUPPORT?
(this[t]=e>>>8,this[t+1]=255&e):I(this,e,t,!1)
,t+2},u.prototype.writeInt32LE=function(e,t,r)
{return
e=+e,t|=0,r||P(this,e,t,4,2147483647,-21474836
48),u.TYPED_ARRAY_SUPPORT?
(this[t]=255&e,this[t+1]=e>>>8,this[t+2]=e>>>1
6,this[t+3]=e>>>24):B(this,e,t,!0),t+4},u.prot
otype.writeInt32BE=function(e,t,r){return
e=+e,t|=0,r||P(this,e,t,4,2147483647,-21474836
48),e<0&&
(e=4294967295+e+1),u.TYPED_ARRAY_SUPPORT?
(this[t]=e>>>24,this[t+1]=e>>>16,this[t+2]=e>>
>8,this[t+3]=255&e):B(this,e,t,!1),t+4},u.prot
otype.writeFloatLE=function(e,t,r){return
j(this,e,t,!0,r)},u.prototype.writeFloatBE=fun
ction(e,t,r){return
j(this,e,t,!1,r)},u.prototype.writeDoubleLE=fu
nction(e,t,r){return
N(this,e,t,!0,r)},u.prototype.writeDoubleBE=fu
nction(e,t,r){return
N(this,e,t,!1,r)},u.prototype.copy=function(e,
t,r,n){if(r||(r=0),n||0===n||
(n=this.length),t>=e.length&&(t=e.length),t||
(t=0),n>0&&n<r&&(n=r),n===r)return
0;if(0===e.length||0===this.length)return
0;if(t<0)throw new RangeError("targetStart out
of bounds");if(r<0||r>=this.length)throw new
RangeError("sourceStart out of
bounds");if(n<0)throw new
RangeError("sourceEnd out of
bounds");n>this.length&&
(n=this.length),e.length-t<n-r&&(n=e.length-
t+r);var i,o=n-
r;if(this===e&&r<t&&t<n)for(i=o-1;i>=0;--
i)e[i+t]=this[i+r];else
if(o<1e3||!u.TYPED_ARRAY_SUPPORT)for(i=0;i<o;+
+i)e[i+t]=this[i+r];else
Uint8Array.prototype.set.call(e,this.subarray(
r,r+o),t);return
o},u.prototype.fill=function(e,t,r,n)
{if("string"==typeof e){if("string"==typeof t?
(n=t,t=0,r=this.length):"string"==typeof r&&
(n=r,r=this.length),1===e.length){var
i=e.charCodeAt(0);i<256&&(e=i)}if(void
0!==n&&"string"!=typeof n)throw new
TypeError("encoding must be a
string");if("string"==typeof
n&&!u.isEncoding(n))throw new
TypeError("Unknown encoding:
"+n)}else"number"==typeof e&&
(e&=255);if(t<0||this.length<t||this.length<r)
throw new RangeError("Out of range
index");if(r<=t)return this;var
o;if(t>>>=0,r=void 0===r?this.length:r>>>0,e||
(e=0),"number"==typeof
e)for(o=t;o<r;++o)this[o]=e;else{var
s=u.isBuffer(e)?e:D(new
u(e,n).toString()),a=s.length;for(o=0;o<r-
t;++o)this[o+t]=s[o%a]}return this};var
U=/[^+\/0-9A-Za-z-_]/g;function q(e){return
e<16?"0"+e.toString(16):e.toString(16)}functio
n D(e,t){var r;t=t||1/0;for(var
n=e.length,i=null,o=[],s=0;s<n;++s)
{if((r=e.charCodeAt(s))>55295&&r<57344){if(!i)
{if(r>56319){(t-
=3)>-1&&o.push(239,191,189);continue}if(s+1===
n){(t-
=3)>-1&&o.push(239,191,189);continue}i=r;conti
nue}if(r<56320){(t-
=3)>-1&&o.push(239,191,189),i=r;continue}r=655
36+(i-55296<<10|r-56320)}else i&&(t-
=3)>-1&&o.push(239,191,189);if(i=null,r<128)
{if((t-=1)<0)break;o.push(r)}else if(r<2048)
{if((t-=2)
<0)break;o.push(r>>6|192,63&r|128)}else
if(r<65536){if((t-=3)
<0)break;o.push(r>>12|224,r>>6&63|128,63&r|128
)}else{if(!(r<1114112))throw new
Error("Invalid code point");if((t-=4)
<0)break;o.push(r>>18|240,r>>12&63|128,r>>6&63
|128,63&r|128)}}return o}function H(e){return
n.toByteArray(function(e){if((e=function(e)
{return e.trim?
e.trim():e.replace(/^\s+|\s+$/g,"")}
(e).replace(U,"")).length<2)return"";for(;e.le
ngth%4!=0;)e+="=";return e}(e))}function
z(e,t,r,n){for(var i=0;i<n&&!
(i+r>=t.length||i>=e.length);++i)t[i+r]=e[i];r
eturn i}}).call(this,r(6))},function(e,t)
{"function"==typeof Object.create?
e.exports=function(e,t){t&&
(e.super_=t,e.prototype=Object.create(t.protot
ype,{constructor:
{value:e,enumerable:!1,writable:!0,configurabl
e:!0}}))}:e.exports=function(e,t){if(t)
{e.super_=t;var r=function()
{};r.prototype=t.prototype,e.prototype=new
r,e.prototype.constructor=e}}},function(e,t,r)
{"use strict";r.d(t,"b",(function(){return
256})),r.d(t,"g",(function(){return
256})),r.d(t,"a",(function(){return"AES-
CBC"})),r.d(t,"f",(function(){return"SHA-
256"})),r.d(t,"e",(function()
{return"HMAC"})),r.d(t,"i",(function()
{return"SHA-256"})),r.d(t,"j",(function()
{return"SHA-512"})),r.d(t,"h",(function()
{return 512})),r.d(t,"d",(function()
{return"encrypt"})),r.d(t,"c",(function()
{return"decrypt"})),r.d(t,"k",(function()
{return"sign"})),r.d(t,"l",(function()
{return"verify"}))},function(e,t){var
r,n,i=e.exports={};function o(){throw new
Error("setTimeout has not been
defined")}function s(){throw new
Error("clearTimeout has not been
defined")}function a(e)
{if(r===setTimeout)return
setTimeout(e,0);if((r===o||!r)&&setTimeout)ret
urn r=setTimeout,setTimeout(e,0);try{return
r(e,0)}catch(t){try{return
r.call(null,e,0)}catch(t){return
r.call(this,e,0)}}}!function()
{try{r="function"==typeof setTimeout?
setTimeout:o}catch(e)
{r=o}try{n="function"==typeof clearTimeout?
clearTimeout:s}catch(e){n=s}}();var u,c=
[],f=!1,h=-1;function l(){f&&u&&
(f=!1,u.length?
c=u.concat(c):h=-1,c.length&&d())}function d()
{if(!f){var e=a(l);f=!0;for(var t=c.length;t;)

