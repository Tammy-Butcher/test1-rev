---
title: Rev Device Guides
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: the-rev-home-page
      title: The Rev Home Page
    - type: basic
      slug: rev-video-guides
      title: Rev Video Guides
    - type: basic
      slug: rev-event-guides
      title: Rev Event Guides
    - type: basic
      slug: rev-channel-guides
      title: Rev Channel Guides
    - type: basic
      slug: configure-access-and-permissions
      title: Rev Access and Security Guides
    - type: basic
      slug: rev-branding-and-style-guides
      title: Rev Branding and Style Guides
    - type: basic
      slug: analytics-and-reports-guides
      title: Analytics and Reports Guides
    - type: basic
      slug: supported-video-and-audio-formats
      title: Video and Audio Formats
    - type: basic
      slug: rev-integration-guides
      title: Rev Integration Guides
---
Devices are external components that “talk” to Rev and may include Vbrick Encoders/Decoders, Distributed Media Engines (DMEs), LDAP servers, and Set Top Boxes. Once configured, devices are placed in zones.  Using devices and zones in Rev, you are able to maintain strict control of your network, bandwidth, and content ingestion easily and intuitively.

This set of guides explains how to link and configure the various devices that work with Rev and then place them in zone hierarchies to set up your entire streaming ecosystem.

<HTMLBlock>{`
<link
	href="https://fonts.googleapis.com/icon?family=Material+Icons"
	rel="stylesheet"
/>
<link
	href="https://fonts.googleapis.com/css?family=Open+Sans:400,600"
	rel="stylesheet"
/>

<div class="card-menu">
	<div class="card">
		<div class="card-header">Devices</div>
		<div class="card-main">
			<i class="material-icons">timeline</i>
			<div class="main-description">
				<a href="/docs/getting-started-with-rev-devices">Initial Setup</a>
			</div>
		</div>
	</div>

	<div class="card">
		<div class="card-header">Devices</div>
		<div class="card-main">
			<i class="material-icons">devices_other</i>
			<div class="main-description">
				<a href="/docs/add-a-source-or-custom-device"
					>Add a Source or Custom Device</a
				>
			</div>
		</div>
	</div>

	<div class="card">
		<div class="card-header">Devices</div>
		<div class="card-main">
			<i class="material-icons">source</i>
			<div class="main-description">
				<a href="/docs/use-ldap-and-active-directory-with-rev"
					>Use LDAP & Active Directory</a
				>
			</div>
		</div>
	</div>

	<div class="card">
		<div class="card-header">Devices</div>
		<div class="card-main">
			<i class="material-icons">date_range</i>
			<div class="main-description">
				<a href="/docs/add-a-presentation-profile">Add Presentation Profiles</a>
			</div>
		</div>
	</div>

	<div class="card">
		<div class="card-header">Devices</div>
		<div class="card-main">
			<i class="material-icons">device_hub</i>
			<div class="main-description">
				<a href="/docs/manage-dme-devices">Manage & Add DMEs</a>
			</div>
		</div>
	</div>

	<div class="card">
		<div class="card-header">Devices</div>
		<div class="card-main">
			<i class="material-icons">devices</i>
			<div class="main-description">
				<a href="/docs/add-a-set-top-box-or-additional-display-device"
					>Set Up Display Devices & Set Top Boxes</a
				>
			</div>
		</div>
	</div>

	<div class="card">
		<div class="card-header">Zones</div>
		<div class="card-main">
			<i class="material-icons">mediation</i>
			<div class="main-description">
				<a href="/docs/manage-and-add-zones">Configure Rev Zones</a>
			</div>
		</div>
	</div>

	<div class="card">
		<div class="card-header">Devices</div>
		<div class="card-main">
			<i class="material-icons">engineering</i>
			<div class="main-description">
				<a href="/docs/device-maintenance">Device Maintenance</a>
			</div>
		</div>
	</div>
</div>

<style>
	body {
		font-family: "Open Sans", sans-serif;
	}

	.card-menu {
		display: flex;
		flex-flow: row wrap;
		justify-content: center;
		align-items: middle;
	}

	.card {
		width: 150px; 
		display: flex; 
		flex-direction: column; 
		border: 1px solid #4fb9e7; 
		border-radius: 4px; 
		overflow: hidden; 
		margin: 5px; 
	}

	.card:hover {
		box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
	}

	.card-header {
		color: #1d9dd5;
		text-align: center;
		font-size: 12px;
		font-weight: 600;
		border-bottom: 1px solid #7ccbed;
		background-color: #b8e3f5;
		padding: 5px 10px;
	}

	.card-main {
		display: flex; 
		flex-direction: column; 
		justify-content: center; 
		align-items: center; 
		padding: 15px 0; 
	}

	.material-icons {
		font-size: 36px;
		color: #1d9dd5;
		margin-bottom: 5px;
	}

	.main-description {
		color: #1d9dd5;
		font-size: 12px;
		text-align: center;
		text-decoration: none;
	}

	.main-description a {
		text-decoration: none;
		color: #1d9dd5;
	}
</style>
`}</HTMLBlock>
