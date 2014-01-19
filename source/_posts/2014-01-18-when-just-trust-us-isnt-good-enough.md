---
layout: post
title: "When \"Just Trust Us\" Isn't Good Enough"
date: 2014-01-18 17:16:29 -0800
comments: true
categories: net-neutrality
---

*I originally wrote this paper for an interdisciplinary Ethics and Technology course, during the fall of 2013.*
      
Net neutrality is a term frequently encountered when discussing access to information on the Internet. While it is generally intended to refer to a guarantee of certain qualities of access to the global Internet, it has been specifically defined in many different ways. I intend to ethically analyze the various aspects of net neutrality, including several common definitions. I will contend that a definition of net neutrality that allows for network traffic prioritization and shaping is ethical, but only for the purposes of managing and improving the network. Non-net neutrality is unethical if it is done for financial gain (e.g. “pay extra for the premium sites package”), if it is not transparent to the end user, or is done to discriminate against a particular class of users.

<!--more-->

Before any critical and ethical analysis of net neutrality can be made, we must first understand what the term “net neutrality” means. There are a number of definitions in wide use, each with a slightly different point of view as to what does and does not constitute net neutrality. We will briefly explore several of these before arriving at a definition that will be used in the remainder of this analysis.
  
The term net neutrality was first used by Tim Wu[^1], Professor of Law at Columbia University. The most basic definition of net neutrality adopted by Wu is as a principle applicable to network design: 

{% blockquote %}
A maximally useful public information network aspires to treat all content, sites, and platforms equally (Wu, 2003). 
{% endblockquote %}

To support this definition, Wu describes, as an example of a neutral network, the public electricity grid. The electricity grid is designed to be end-use agnostic, allowing any device to utilize it. The utility company responsible for designing and maintaining the grid does not design the network for any particular use or device, but rather operates it on the principle of neutral, general purpose use. (The electrical network is obviously not an “information network,” but the metaphor is still useful to clarify Wu's definition.)

Another definition, more specific to Internet computer networks, is put forth by Krämer *et al*[^2] in “Net Neutrality Progress”: 

{% blockquote %}
Net neutrality prohibits Internet service providers from speeding up, slowing down or blocking Internet traffic based on its source, ownership or destination (Krämer et al).
{% endblockquote %}

It is important to note here the differences between this definition, referred to as “strict network neutrality”, and the general definition adopted by Wu. The definition used in Krämer *et al* allows for differing treatment of broad categories of Internet traffic in order to manage various forms of content with different requirements (e.g. low latency requirements for Internet voice communication versus the relative insensitivity to latency exhibited by peer-to-peer download systems). Wu's definition of a maximally useful public information network does not allow for such discrimination, even when discrimination is useful as a tool to improve the quality of service to the majority of users of a network without significantly reducing the quality of service provided to the minority. I will explore the use of non-net neutrality as a tool to improve the quality of the network later in this paper. 

A third, even more specific, definition of net neutrality is provided by Hahn *et al*[^3] in “The Economics of Net Neutrality.” They claim that net neutrality means that:

{% blockquote %}
Broadband service providers charge consumers only once for Internet access, do not favor one content provider over another, and do not charge content providers for sending information over broadband lines to end users (Hahn et al).
{% endblockquote %}

The model where service providers do charge content providers for sending information to end users is referred to by Krämer *et al* as the “termination fee model.” This model is of interest because of its potential to adversely affect certain types of services. For example, providers of streaming video, by the nature of their product, generate much more network traffic than providers of textual content. This does not imply that one type of content is intrinsically better or more useful, but under a termination fee model, content providers whose service requires more network traffic may have to pay significantly more to reach consumers. 

The remainder of this analysis will use the definition of net neutrality given by Krämer *et al*, with the addendum that any practices that cause anything but strict and total equality in the treatment of network traffic must be transparently and effectively communicated to the consumers affected. From an ethical perspective, this is the most defensible of the three definitions given above.  We will explore in greater depth the issues inherent in the definitions of network neutrality provided by Tim Wu and Hahn *et al*, as well as outline why the principle of net neutrality as defined in Krämer *et al* is an important concept to uphold when setting policy and designing legislation.

To ethically analyze the issue of net neutrality, it is first useful to assert that the Internet as a resource for obtaining, creating, and sharing information is a service that can have an enormously positive effect on humanity. The Internet was created from a vision of an idealized, decentralized, democratic inter-network of computers. It has increasingly become a tool to enfranchise people. On the Internet, in theory, any person has the tools needed to express their view. Small businesses can compete on a level playing field with entrenched monopolies. People in countries with oppressive social and political policies can use the Internet to anonymously advocate for positive change. However, these benefits can only be retained and expanded if the principles of non-discrimination given by net neutrality can be upheld. 

The definition of net neutrality adopted above does not claim that all network traffic must be treated with total equality. In fact, such a policy would be inimical to the goal of providing everyone with an equal opportunity to benefit from the Internet. The issue is primarily technical. Different categories of network traffic have different requirements, and place different levels of demand on the network of the service provider. As alluded to above, real-time voice communication over the Internet (voice over Internet Protocol, or VoIP) is relatively bandwidth unintensive. However, VoIP communication is very strongly dependent on low levels of latency (the speed at which one single piece of data can travel from the source to the destination). On the other hand, peer-to-peer (P2P) file sharing protocols are extremely bandwidth intensive, while being essentially unaffected by high levels of latency. If a principle of strict traffic equality is adhered to, a user attempting to utilize VoIP will be harmed by a user utilizing peer-to-peer file sharing on the network. This is contrary to the principle of fair and equal access: the VoIP user is unfairly penalized, while the P2P user gains no benefit.

In this situation, a policy that prioritizes VoIP traffic over traffic generated by the P2P user is the correct option. The amount of bandwidth used by the prioritized VoIP user is minimally impacts the experience of  the P2P user, while dramatically increasing the experience of that VoIP user. The end result is that both users are granted fair and useful access to the network.

Service providers that adopt such measures, however, must be carefully monitored to ensure that such traffic management is done strictly to ensure the equality of all types of network communication. The temptation in a market where service providers are profit-driven is that competitive service providers will use traffic shaping and prioritization for financial gain, at the expense of consumers. We have already encountered one of these scenarios in the so-called termination fee model, where content providers may be unfairly discriminated against due to the nature of their content's delivery requirements. 

Another possible scenario inimical to the interests of Internet users is that of the “cable television” model. In this situation, service providers may begin offering consumers predetermined packages of Internet content access. For example, a service provider may offer a “Basic Internet” package, allowing users access to a handful of popular, preselected sites. Access to other sites is only granted if the user pays for the “Premium Internet” package. This scenario is problematic in that it disenfranchises content producers who are not among the list of preselected, popular Internet content providers.

Issues related to deliberate discrimination and suppression of speech must also be carefully watched for. Under the guise of network traffic management, it is easy to envision a scenario where a service provider unfairly degrades or even blocks content that is distasteful to its controlling interests, whether that distaste arises from political, moral, or financial reasons. While there may be no legal protection for unwanted speech on private networks in this country, such discrimination is contrary to the ethical ideals of the Internet, and should be avoided in order to promote the benefits of ubiquitous inter-networking for everyone.

The final component of an ethical application of net neutrality is that any action taken by a service provider beyond strict, unmanaged equality of all network traffic must be transparently and effectively communicated to any users affected. It is difficult to accept that a service provider is protecting the interests of the network users if traffic is manipulated in secrecy. Such concerns are not merely theoretical. In 2007, it was revealed that Comcast, a large Internet service provider, was routinely throttling traffic using the BitTorrent peer-to-peer file sharing protocol (Wired, 2008)[^4]. The throttling was done secretly, and was targeted at a specific application of the Internet. It continues to remain unclear whether that traffic shaping was done for the purpose of improving the experience of all users of the network, or whether there was another motivation. It is certainly possible that Comcast was protecting the interests of users who may have been adversely affected by BitTorrent traffic. However, Comcast is also a large provider to cable television services, which are often seen to be in competition with P2P sources of media. Comcast's deliberate secrecy over the practice of throttling such traffic causes significant suspicion of ulterior motives. 

Clearly, net neutrality is a complex issue with many ethical facets. I have argued an ethical definition of net neutrality that attempts to level the playing field for all users of the Internet, a definition that disallows discrimination based on source, destination, and owner. Additionally, for a policy of network traffic management to be ethically sound, any actions taken by the service provider must be open and transparent to any user affected by such actions. To maintain an open, fair, and beneficial Internet any actions taken by service providers that fail to meet these criteria should be viewed with immediate suspicion.


[^1]: Wu, Tim. "Network Neutrality FAQ." Network Neutrality FAQ. N.p., n.d. Web. 03 Dec. 2013. <http://timwu.org/network_neutrality.html>.

[^2]: Kraemer, Jan and Wiewiorra, Lukas and Weinhardt, Christof, Net Neutrality: A Progress Report (October 24, 2013). Telecommunications Policy 37(9). 794–813.. Available at SSRN: <http://ssrn.com/abstract=2344623> or <http://dx.doi.org/10.2139/ssrn.2344623>

[^3]: Hahn, Robert W. and Wallsten, Scott, The Economics of Net Neutrality (April 2006). AEI-Brookings Joint Center Working Paper No. RP06-13. Available at SSRN: <http://ssrn.com/abstract=943757> or <http://dx.doi.org/10.2139/ssrn.94375>

[^4]: Kravets, David. "Comcast Discloses Throttling Practices — BitTorrent Targeted."Wired.com. Conde Nast Digital, 19 Sept. 2008. Web. 03 Dec. 2013. <http://www.wired.com/threatlevel/2008/09/comcast-disclos/>.
