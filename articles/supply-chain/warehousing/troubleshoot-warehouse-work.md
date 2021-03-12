---
title: استكشاف أخطاء عمل المستودع وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمل المستودعات في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970221"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="8ab43-103">استكشاف أخطاء عمل المستودع وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="8ab43-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ab43-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمل المستودعات في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8ab43-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="8ab43-105">لا يمكن نقل لوحات الترخيص التي تحتوي علي أصناف أرقام تسلسليه عند السماح بإصدار فارغ وإيصال فارغ في مجموعه ابعاد التعقب.</span><span class="sxs-lookup"><span data-stu-id="8ab43-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ab43-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8ab43-106">Issue description</span></span>

<span data-ttu-id="8ab43-107">لا يمكنك نقل لوحه ترخيص باستخدام عنصر قائمه **الحركة** إذا كان الرقم المسلسل يحتوي علي إعدادات *لإصدار فارغ مسموح به* و *تم السماح بإيصال فارغ* في مجموعه بعد التعقب، وإذا كان هناك عده لوحات ترخيص في نفس الموقع ، يكون لبعضها الأرقام التسلسلية وبعضها لا تملكها.</span><span class="sxs-lookup"><span data-stu-id="8ab43-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ab43-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8ab43-108">Issue resolution</span></span>

<span data-ttu-id="8ab43-109">سيتم حل هذه المشكلة من خلال التغييرات التي يتم نشرها في [قاعدة المعارف 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="8ab43-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="8ab43-110">ستؤدي هذه التغييرات إلى جعل حقل **الرقم التسلسلي** اختياريا عند السماح بالاستلام الفارغ والإصدار الفارغ.</span><span class="sxs-lookup"><span data-stu-id="8ab43-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="8ab43-111">أتلقى رسالة الخطا التالية في تطبيق المستودع عند معالجه الحركات: "مالك المخزون غير %1مسموح به في هذه العملية."</span><span class="sxs-lookup"><span data-stu-id="8ab43-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ab43-112">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8ab43-112">Issue description</span></span>

<span data-ttu-id="8ab43-113">بعد تتبع **المالك** لا يكون موجودا عند استخدام تطبيق المستودع لعمل الحركات.</span><span class="sxs-lookup"><span data-stu-id="8ab43-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="8ab43-114">يظهر دفتر يوميه تحويل المخزون العادي من عميل Supply Chain Management للعمل كما يجب ولا يمكن ترحيله الا إذا تم ملء بعد **المالك**.</span><span class="sxs-lookup"><span data-stu-id="8ab43-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ab43-115">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8ab43-115">Issue resolution</span></span>

<span data-ttu-id="8ab43-116">قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه.</span><span class="sxs-lookup"><span data-stu-id="8ab43-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="8ab43-117">تدعم عمليات أداره المستودع حاليا المخزون الذي يملكه الكيان القانوني فقط.</span><span class="sxs-lookup"><span data-stu-id="8ab43-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
