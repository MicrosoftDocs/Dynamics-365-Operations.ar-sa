---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR(24 سبتمبر 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e0c1a3bf7613db4887e0943a70ad6262a70997f0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898956"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="4c870-103">ما الجديد أو المتغير في Dynamics 365 Talent - Core HR(24 سبتمبر 2018)</span><span class="sxs-lookup"><span data-stu-id="4c870-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

<span data-ttu-id="4c870-104">**الإصدار 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="4c870-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="4c870-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="4c870-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="4c870-106">تمت إضافة العملة إلى الميزات</span><span class="sxs-lookup"><span data-stu-id="4c870-106">Currency added to Benefits</span></span>

<span data-ttu-id="4c870-107">تم تحديث خطط الميزات لتضمين عملة الميزة.</span><span class="sxs-lookup"><span data-stu-id="4c870-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="4c870-108">يتوفر هذا الحقل الجديد أيضًا في ميزات العامل المسجلة.</span><span class="sxs-lookup"><span data-stu-id="4c870-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="4c870-109">يمثل هذا الحقل الجديد جزءًا من الاحتفاظ بالميزات وعرض قائمة امتياز أمان الميزات.</span><span class="sxs-lookup"><span data-stu-id="4c870-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="4c870-110">تحديث عملية التناسب- الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="4c870-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="4c870-111">يختلف زمن توقف منح المؤسسات استنادًا إلى وقت انضمام الموظفين وتركهم للشركة.</span><span class="sxs-lookup"><span data-stu-id="4c870-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="4c870-112">بالنسبة للموظفين الذين يغادرون المؤسسة، قد يحتاج بعضهم إلى إنهاء المكافأة في تاريخ الإنهاء، في حين يعتمد الآخرين على أخر يوم عمل لوقف عملية الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="4c870-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="4c870-113">توفر هذه التغييرات للمؤسسات إمكانية الاختيار وقت إنهاء التسجيل خلال عملية الإنهاء.</span><span class="sxs-lookup"><span data-stu-id="4c870-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="4c870-114">تمثل هذه الخيارات الجديدة جزءًا من الامتيازات لإنهاء عامل وإنهاء عامل من إدارة الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="4c870-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="4c870-115">التغييرات الأخرى</span><span class="sxs-lookup"><span data-stu-id="4c870-115">Other changes</span></span>

<span data-ttu-id="4c870-116">يشمل هذا الإصدار عددًا من إصلاحات الأخطاء الإضافية.</span><span class="sxs-lookup"><span data-stu-id="4c870-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="4c870-117">مشكلات معروفة​</span><span class="sxs-lookup"><span data-stu-id="4c870-117">Known Issue</span></span>

-   <span data-ttu-id="4c870-118">**مشكلة:** عند إضافة مرفق جديد لعامل، تتحول الأزرار **جديد** و **تحرير** إلى اللون الرمادي. **حل بديل:** قبل فتح صفحة المرفق، تأكد أن مربعات الحقائق في صفحة **العامل** مغلقة.</span><span class="sxs-lookup"><span data-stu-id="4c870-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="4c870-119">إذا تم إغلاق مربعات الحقائق عندما يتم تحميل صفحة **العامل**، فسوف يتم تمكين أزرار المرفقات.</span><span class="sxs-lookup"><span data-stu-id="4c870-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="4c870-120">(سوف يتم إصلاح هذه المشكلة في التحديث التالي للنظام الأساسي.)</span><span class="sxs-lookup"><span data-stu-id="4c870-120">(This issue will be fixed in the next platform update.)</span></span>
