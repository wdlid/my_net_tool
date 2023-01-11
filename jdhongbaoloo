const CHECK_URL = 'api.m.jd.com/client.actions'

const url = $request.url
const isCheckUrl = (url) => url.includes(CHECK_URL)

const getbalance = (url) => url.includes('myhongbao_getHongBaoBalance')
const getusableHonglist = (url) => url.includes('getUsableHongBaoList')

if (getbalance(url) && $response.status == 200) {
  const unlock = {"balanceMap":{"totalUsableBalance":17.33,"allLimitOrgBalance":0,"totalPreBalance":0,"totalCurrentBalance":17.33,"allOrgBalance":17.33,"totalDisableBalance":0},"count":1,"message":"查询成功！祝您购物愉快~","resultCode":200,"success":true,"tid":0,"totalBalance":17.33}

  const status = 200
  const headers = $response.headers
  const body = JSON.stringify(unlock)

  $done({ status, headers, body })
} else {
  $done({})
}
