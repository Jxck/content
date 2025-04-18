---
title: RTCIceCandidatePairStats
slug: Web/API/RTCIceCandidatePairStats
page-type: web-api-interface
browser-compat: api.RTCStatsReport.type_candidate-pair
---

{{APIRef("WebRTC")}}

The **`RTCIceCandidatePairStats`** dictionary of the [WebRTC API](/en-US/docs/Web/API/WebRTC_API) is used to report statistics that provide insight into the quality and performance of an {{domxref("RTCPeerConnection")}} while connected and configured as described by the specified pair of {{Glossary("ICE")}} candidates.

The statistics can be obtained by iterating the {{domxref("RTCStatsReport")}} returned by {{domxref("RTCPeerConnection.getStats()")}} until you find an entry with the [`type`](/en-US/docs/Web/API/RTCIceCandidatePairStats/type) of `"candidate-pair"`.

## Instance properties

- {{domxref("RTCIceCandidatePairStats.availableIncomingBitrate", "availableIncomingBitrate")}} {{optional_inline}} <!-- Not in BCD but is in spec IDL. -->
  - : A number representing the available inbound capacity of the network.
    This reports the total number of bits per second available for all of the candidate pair's incoming {{Glossary("RTP")}} streams.
    It does not take into account the size of the Internet Protocol (IP) overhead, nor any other transport layers such as {{Glossary("TCP")}} or {{Glossary("UDP")}}.
- {{domxref("RTCIceCandidatePairStats.availableOutgoingBitrate", "availableOutgoingBitrate")}} {{optional_inline}}
  - : A number representing the approximate available outbound capacity of the network.
    This reports the total number of bits per second available for all of the candidate pair's outgoing {{Glossary("RTP")}} streams.
    It does not take into account the size of the IP overhead, nor any other transport layers such as {{Glossary("TCP")}} or {{Glossary("UDP")}}.
- {{domxref("RTCIceCandidatePairStats/bytesDiscardedOnSend", "bytesDiscardedOnSend")}} {{optional_inline}} {{experimental_inline}}
  - : An integer representing the total number of bytes discarded due to socket errors on this candidate pair.
- {{domxref("RTCIceCandidatePairStats/bytesReceived", "bytesReceived")}} {{optional_inline}}
  - : An integer representing the total number of payload bytes received on this candidate pair.
- {{domxref("RTCIceCandidatePairStats.bytesSent", "bytesSent")}} {{optional_inline}}
  - : An integer representing the total number of payload bytes sent on this candidate pair (the total number of bytes sent excluding any headers, padding, or other protocol overhead).
- {{domxref("RTCIceCandidatePairStats/consentRequestsSent", "consentRequestsSent")}} {{optional_inline}} {{experimental_inline}}
  - : An integer representing the total number of [STUN](/en-US/docs/Web/API/WebRTC_API/Protocols#stun) consent requests sent on this candidate pair.
- {{domxref("RTCIceCandidatePairStats.currentRoundTripTime", "currentRoundTripTime")}} {{optional_inline}}
  - : A number representing the total time, in seconds, that elapsed between the most recently-sent STUN request and the response being received.
    This may be based upon requests that were involved in confirming permission to open the connection.
- {{domxref("RTCIceCandidatePairStats.lastPacketReceivedTimestamp", "lastPacketReceivedTimestamp")}} {{optional_inline}}
  - : A {{domxref("DOMHighResTimeStamp")}} value indicating the time at which the last packet was received by the local peer from the remote peer for this candidate pair. Timestamps are not recorded for STUN packets.
- {{domxref("RTCIceCandidatePairStats.lastPacketSentTimestamp", "lastPacketSentTimestamp")}} {{optional_inline}}
  - : A {{domxref("DOMHighResTimeStamp")}} value indicating the time at which the last packet was sent from the local peer to the remote peer for this candidate pair. Timestamps are not recorded for STUN packets.
- {{domxref("RTCIceCandidatePairStats.localCandidateId", "localCandidateId")}} {{optional_inline}}
  - : A string representing the unique ID corresponding to the {{domxref("RTCIceCandidate")}} from the data included in the {{domxref("RTCIceCandidateStats")}} object providing statistics for the candidate pair's local candidate.
- {{domxref("RTCIceCandidatePairStats.nominated", "nominated")}} {{optional_inline}}
  - : A Boolean value which, if `true`, indicates that the candidate pair described by this object is one which has been proposed for use, and will be (or was) used if its priority is the highest among the nominated candidate pairs. See {{RFC(5245, "", "7.1.3.2.4")}} for details.
- {{domxref("RTCIceCandidatePairStats/packetsDiscardedOnSend", "packetsDiscardedOnSend")}} {{optional_inline}} {{experimental_inline}}
  - : An integer representing the total number of packets discarded due to socket errors on this candidate pair.
- {{domxref("RTCIceCandidatePairStats/packetsReceived", "packetsReceived")}} {{optional_inline}} {{experimental_inline}}
  - : An integer representing the total number of packets received on this candidate pair.
- {{domxref("RTCIceCandidatePairStats/packetsSent", "packetsSent")}} {{optional_inline}} {{experimental_inline}}
  - : An integer representing the total number of packets sent on this candidate pair.
- {{domxref("RTCIceCandidatePairStats.remoteCandidateId", "remoteCandidateId")}} {{optional_inline}}
  - : A string containing a unique ID corresponding to the remote candidate from which data was taken to construct the `RTCIceCandidateStats` object describing the remote end of the connection.
- {{domxref("RTCIceCandidatePairStats.requestsReceived", "requestsReceived")}} {{optional_inline}}
  - : An integer representing the total number of connectivity check requests that have been received, including retransmissions. This value includes both connectivity checks and STUN consent checks.
- {{domxref("RTCIceCandidatePairStats.requestsSent", "requestsSent")}} {{optional_inline}}
  - : An integer representing the total number of connectivity check requests that have been sent, _not_ including retransmissions.
- {{domxref("RTCIceCandidatePairStats.responsesReceived", "responsesReceived")}} {{optional_inline}}
  - : An integer representing the total number of connectivity check responses that have been received.
- {{domxref("RTCIceCandidatePairStats.responsesSent", "responsesSent")}} {{optional_inline}}
  - : An integer representing the total number of connectivity check responses that have been sent. This includes both connectivity check requests and STUN consent requests.
- {{domxref("RTCIceCandidatePairStats.state", "state")}} {{optional_inline}}
  - : A string which indicates the state of the connection between the two candidates.
- {{domxref("RTCIceCandidatePairStats.totalRoundTripTime", "totalRoundTripTime")}} {{optional_inline}}
  - : A number indicating the total time, in seconds, that has elapsed between sending STUN requests and receiving responses to them, for all such requests made to date on this candidate pair.
    This includes both connectivity check and consent check requests. You can compute the average round trip time (RTT) by dividing this value by {{domxref("RTCIceCandidatePairStats.responsesReceived", "responsesReceived")}}.
- {{domxref("RTCIceCandidatePairStats.transportId", "transportId")}} {{optional_inline}}
  - : A string that uniquely identifies the {{domxref("RTCIceTransport")}} that was inspected to obtain the transport-related statistics (as found in {{domxref("RTCTransportStats")}}) used in generating this object.

### Common instance properties

The following properties are common to all WebRTC statistics objects.

<!-- RTCStats -->

- {{domxref("RTCIceCandidatePairStats.id", "id")}}
  - : A string that uniquely identifies the object that is being monitored to produce this set of statistics.
- {{domxref("RTCIceCandidatePairStats.timestamp", "timestamp")}}
  - : A {{domxref("DOMHighResTimeStamp")}} object indicating the time at which the sample was taken for this statistics object.
- {{domxref("RTCIceCandidatePairStats.type", "type")}}
  - : A string with the value `"candidate-pair"`, indicating the type of statistics that the object contains.

### Deprecated properties

The following properties have been removed from the specification and should no longer be used.
You should update any existing code to avoid using them as soon as is practical.
Check the [compatibility table](#browser_compatibility) for details on which browsers support them and in which versions.

- {{domxref("RTCIceCandidatePairStats.priority", "priority")}} {{Deprecated_Inline}} {{optional_inline}} {{non-standard_inline}}
  - : An integer value indicating the candidate pair's priority.
- {{domxref("RTCIceCandidatePairStats.readable", "readable")}} {{Deprecated_Inline}} {{optional_inline}} {{Non-standard_Inline}}
  - : A Boolean value indicating whether or not data can be sent over the connection described by the candidate pair.
- {{domxref("RTCIceCandidatePairStats.writable", "writable")}} {{Deprecated_Inline}} {{optional_inline}} {{Non-standard_Inline}}
  - : A Boolean value indicating whether or not data can be received on the connection described by the candidate pair.

### Non-standard properties

- {{domxref("RTCIceCandidatePairStats.selected", "selected")}} {{Non-standard_Inline}} {{optional_inline}}
  - : A Firefox-specific Boolean value which is `true` if the candidate pair described by this object is the one currently in use.
    The spec-compliant way to determine the selected candidate pair is to look for a stats object of type `transport`, which is an {{domxref("RTCTransportStats")}} object.
    That object's {{domxref("RTCTransportStats.selectedCandidatePairId", "selectedCandidatePairId")}} property indicates whether or not the specified transport is the one being used.

## Usage notes

The currently-active ICE candidate pair—if any—can be obtained by calling the {{domxref("RTCIceTransport")}} method {{domxref("RTCIceTransport.getSelectedCandidatePair", "getSelectedCandidatePair()")}}, which returns an {{domxref("RTCIceCandidatePair")}} object, or `null` if there isn't a pair selected.
The active candidate pair describes the current configuration of the two ends of the {{domxref("RTCPeerConnection")}}.

Any candidate pair that isn't the active pair of candidates for a transport gets deleted if the {{domxref("RTCIceTransport")}} performs an ICE restart, at which point the {{domxref("RTCIceTransport.state", "state")}} of the ICE transport returns to `new` and negotiation starts once again.
For more information, see [ICE restart](/en-US/docs/Web/API/WebRTC_API/Session_lifetime#ice_restart).

## Example

This example computes the average time elapsed between connectivity checks.

```js
if (rtcStats && rtcStats.type === "candidate-pair") {
  let elapsed =
    (rtcStats.lastRequestTimestamp - rtcStats.firstRequestTimestamp) /
    rtcStats.requestsSent;

  console.log(`Average time between ICE connectivity checks: ${elapsed} ms.`);
}
```

The code begins by looking at `rtcStats` to see if its {{domxref("RTCIceCandidatePairStats.type", "type")}} is `candidate-pair`.
If it is, then we know that `rtcStats` is in fact an `RTCIceCandidatePairStats` object.
We can then compute the average time elapsed between STUN connectivity checks and log that information.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
