---
title: عدم العثور على مستخدم في "منتقي الأشخاص" في Attract أو Attract
description: يشرح هذا الموضوع الخطوات التي يجب اتخاذها عند عدم ظهور مستخدمين في الشركة في منتقي الأشخاص في Dynamics 365 Talent- Attract أو Onboard
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551923"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a><span data-ttu-id="569ff-103">عدم العثور على مستخدم في "منتقي الأشخاص" في Attract أو Attract</span><span class="sxs-lookup"><span data-stu-id="569ff-103">User not found in People Picker in Attract or Onboard</span></span>
[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="569ff-104">إصدار</span><span class="sxs-lookup"><span data-stu-id="569ff-104">Issue</span></span>

<span data-ttu-id="569ff-105">لا يظهر بعض المستخدمين الموجودين في Microsoft Azure Active Directory (Azure AD) للمستأجر عند البحث عن الاسم في منتقي الأشخاص في Dynamics 365 Talent: Attract أو Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="569ff-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="569ff-106">السبب</span><span class="sxs-lookup"><span data-stu-id="569ff-106">Cause</span></span>

<span data-ttu-id="569ff-107">بعض أنواع المستخدمين غير مدعومة حاليًا في التطبيقين Attract وOnboard.</span><span class="sxs-lookup"><span data-stu-id="569ff-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="569ff-108">تأكد من أن المستخدم ليس مستخدم ضيف متاجرة بين عمل وعمل (B2B) في Azure AD.</span><span class="sxs-lookup"><span data-stu-id="569ff-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="569ff-109">تتوفر معلومات عن "نوع المستخدم" في لوحة Azure Active Directory في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="569ff-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="569ff-110">للحصول على مزيد من المعلومات حول Azure B2B، راجع [ما المقصود بوصول المستخدم الضيف في Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="569ff-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="569ff-111">بالنسبة إلى المستخدمين من غير B2B، قد تكون لدى بعض المستخدمين خاصية "نوع المستخدم" غير كاملة على كائن **المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="569ff-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="569ff-112">يمكن التحقق من هذا الأمر وإصلاحها باستخدام وحدة Azure AD Powershell.</span><span class="sxs-lookup"><span data-stu-id="569ff-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="569ff-113">لمزيد من المعلومات، راجع [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="569ff-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="569ff-114">الدقة</span><span class="sxs-lookup"><span data-stu-id="569ff-114">Resolution</span></span>

<span data-ttu-id="569ff-115">لإكمال الخطوات التالية لحل هذه المشكلة، ستحتاج إلى أذونات "المسؤول العمومي" على مستأجر Azure Active Directory أو أذونات **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="569ff-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="569ff-116">للتحقق من "نوع المستخدم" للمستخدم المتأثر.</span><span class="sxs-lookup"><span data-stu-id="569ff-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="569ff-117">يرجع الأمر المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="569ff-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="569ff-118">لاحظ خاصية **UserType** على المستخدم.</span><span class="sxs-lookup"><span data-stu-id="569ff-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="569ff-119">إذا كانت خاصية **UserType** فارغة، على سبيل المثال، ليست "عضو" أو "ضيف"، فحدّث **UserType** باستخدام الأمر التالي.</span><span class="sxs-lookup"><span data-stu-id="569ff-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
