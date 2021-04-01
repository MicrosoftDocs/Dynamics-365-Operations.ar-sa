---
title: إعداد أسماء دفتر يومية الإيجار
description: يوضح هذا الموضوع كيفية تحديد أسماء دفتر يومية عقد الإيجار. تحدد أسماء دفاتر يومية عقد الإيجار دفاتر اليومية التي تم فيها ترحيل الإدخالات التي تنشأ في تأجير الأصول.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 98595848593e3abd63701b52c7a67ec61288a96e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249619"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="05df6-104">إعداد أسماء دفتر يومية الإيجار</span><span class="sxs-lookup"><span data-stu-id="05df6-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05df6-105">تحدد أسماء دفاتر يومية عقد الإيجار دفاتر اليومية التي تم فيها ترحيل حركات تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="05df6-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="05df6-106">لا تظهر سوي أسماء دفاتر اليومية التي تم تعيينها إلى **تأجير الأصول** لنوع دفتر يومية تأجير الأصول في الحقل **التقييم الأولي** والحقل **اسم دفتر اليومية الشهري** في الصفحة **معلمات تأجير الأصول**</span><span class="sxs-lookup"><span data-stu-id="05df6-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="05df6-107">يمكن تعيين نوع دفتر اليومية **تسجيل فاتورة المورد** إلى الحقل **اسم دفتر يومية الفاتورة** فقط.</span><span class="sxs-lookup"><span data-stu-id="05df6-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="05df6-108">لتكوين أسماء دفاتر يومية عقد الإيجار، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="05df6-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="05df6-109">انتقل إلى **تأجير الأصول‬ \> الإعداد‬ \> معلمات تأجير الأصول**.</span><span class="sxs-lookup"><span data-stu-id="05df6-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="05df6-110">من علامات التبويب **عام**، في الحقل **اسم دفتر يومية التقييم الأولي**، وحدد دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="05df6-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="05df6-111">سيتم ترحيل كافة إدخالات دفتر يومية التقييم الأولي إلى اسم دفتر اليومية هذا.</span><span class="sxs-lookup"><span data-stu-id="05df6-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="05df6-112">في الحقل **اسم دفتر يومية الفاتورة**، حدد دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="05df6-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="05df6-113">في حالة تعيين الخيار **الدفع إلى المورد** إلى **نعم** بالنسبة لدفتر يومية عقد الإيجار، فإنه سيتم ترحيل فواتير دفعات الإيجار والمصروفات إلى اسم دفتر اليومية هذا.</span><span class="sxs-lookup"><span data-stu-id="05df6-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="05df6-114">في الحقل **اسم دفتر يومية عقد الإيجار**، حدد دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="05df6-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="05df6-115">سيتم ترحيل كافة إدخالات الإهلاك والفائدة وإعادة التصنيف قصير الأجل إلى اسم دفتر اليومية هذا.</span><span class="sxs-lookup"><span data-stu-id="05df6-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="05df6-116">في حالة تعيين الخيار **الدفع إلى المورد** إلى **لا** بالنسبة لدفتر يومية عقد الإيجار، فإنه سيتم ترحيل دفعات الإيجار والمصروفات إلى اسم دفتر اليومية هذا.</span><span class="sxs-lookup"><span data-stu-id="05df6-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]