<template>
	<div class="box asideProfile">
		<!-- 个人介绍 -->
		<div class="profile-intro">
			<div class="avatar-box">
				<a href="#">
					<img :src="profile.avatarUrl" alt="" />
				</a>
			</div>
			<div class="user-info">
				<div>
					<span class="name">{{ profile.author }}</span>
				</div>
				<div class="user-info-bottom">
					<span class="year">码龄3年</span>
					<!--                  <span>暂无认证</span>-->
				</div>
			</div>
			<div class="focus-btn">
				<div class="btn" @click="followUser()">
					<a
						href="javascript:;"
						v-if="isShowFollow"
						style="color: #999aaa"
					>已关注</a
					>
					<a href="javascript:;" v-else style="color: #555666">关注</a>
				</div>
			</div>
		</div>
		<!-- 个人数据介绍1 -->
		<div class="data-info">
			<dl>
				<dt class="count">567</dt>
				<dd class="font">原创</dd>
			</dl>
			<dl>
				<dt class="count">21万+</dt>
				<dd class="font">周排名</dd>
			</dl>
			<dl>
				<dt class="count">2万+</dt>
				<dd class="font">总排名</dd>
			</dl>
			<dl>
				<dt class="count">10万+</dt>
				<dd class="font">访问</dd>
			</dl>
			<dl>
				<dt class="count">5</dt>
				<dd class="font">等级</dd>
			</dl>
		</div>
		<!-- 分割线 -->
		<div class="item-rank"></div>
		<!-- 个人数据介绍2 -->
		<div class="data-info">
			<dl>
				<dt class="count">1324</dt>
				<dd class="font">积分</dd>
			</dl>
			<dl>
				<dt class="count">145</dt>
				<dd class="font">粉丝</dd>
			</dl>
			<dl>
				<dt class="count">98</dt>
				<dd class="font">获赞</dd>
			</dl>
			<dl>
				<dt class="count">76</dt>
				<dd class="font">评论</dd>
			</dl>
			<dl>
				<dt class="count">324</dt>
				<dd class="font">收藏</dd>
			</dl>
		</div>
	</div>
</template>

<script>
	export default {
		name: ""
	}
</script>

<style scoped>
	.box {
		/* height: 300px; */
		background-color: #ffffff;
		box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
		margin-bottom: 10px;
	}

	/* 个人box1开始 */
	/* 个人介绍 */
	.profile-intro {
		padding: 16px 16px 6px 16px;
		display: flex;
	}

	.profile-intro .avatar-box {
		position: relative;
		width: 48px;
		height: 48px;
	}

	.profile-intro .avatar-box img {
		display: block;
		width: 48px;
		height: 48px;
		border-radius: 50%;
	}

	.profile-intro .user-info {
		margin-left: 8px;
		width: 156px;
		position: relative;
		padding-top: 4px;
		display: flex;
		flex-direction: column;
	}

	.profile-intro .user-info .name {
		width: 100%;
		font-size: 14px;
		font-weight: 500;
		height: 20px;
		line-height: 20px;
		display: block;
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
	}

	.profile-intro .user-info .user-info-bottom {
		display: flex;
	}

	.profile-intro .user-info .user-info-bottom .year {
		min-width: 62px;
	}

	.profile-intro .user-info .user-info-bottom span {
		color: #999aaa;
		font-size: 13px;
		line-height: 20px;
		height: 20px;
		overflow: hidden;
	}

	/* 数据信息 */
	.data-info {
		display: flex;
		padding: 9px 10px;
	}

	.data-info dl {
		width: 100%;
		text-align: center;
	}

	.data-info dl dt {
		color: #4a4d52;
		font-size: 14px;
		font-weight: 500;
		line-height: 22px;
	}

	.data-info dl dd {
		color: #222226;
		font-size: 14px;
		line-height: 22px;
		padding: 3px 0;
	}

	/* 分割线 */
	.item-rank {
		height: 1px;
		background-color: #f5f6f7;
		width: 268px;
		margin: auto;
	}

	/* 关注 */
	.focus-btn {
		padding: 0px 5px 0px 0px;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.focus-btn .btn {
		font-size: 14px;
		width: 80px;
		height: 28px;
		border-radius: 14px;
		text-align: center;
		color: #555666;
		line-height: 26px;
		border: 1px solid #ccccd8;
		cursor: pointer;
	}

	.focus-btn .btn:hover {
		border: 1px solid #222226;
		/*border: 1px solid #5dcdff;*/
	}

	/* 个人box1结束 */
</style>
